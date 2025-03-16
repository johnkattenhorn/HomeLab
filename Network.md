# HomeLab Network Configuration

## Network Range

- **Network Address:** 192.168.1.0/24
- **Subnet Mask:** 255.255.255.0
- **Gateway:** 192.168.1.1

## Static IP Address Assignments

| Device Name       | IP Address      | MAC Address           |
|-------------------|-----------------|-----------------------|
| Router              | 192.168.1.1     | 00:1A:2B:3C:4D:5E     |
| EdgeServices        | 192.168.1.2     | 00:1A:2B:3C:4D:5F     |
| Server              | 192.168.1.3     | 00:1A:2B:3C:4D:60     |
| Wifi Access Point 1 | 192.168.1.4     | 00:1A:2B:3C:4D:61     |
| Wifi Access Point 2 | 192.168.1.5     | 00:1A:2B:3C:4D:62     |

## DHCP Pool

- **Start Address:** 192.168.1.100
- **End Address:** 192.168.1.200
- **Lease Time:** 24 hours

## Internal DNS

- Internal domain suffix = `kattenhorn.tech`
- References internal IP addresses

## External DNS

- External domain suffix - `kattenhorn.tech`
- References external IP addresses

## Edge Services

Setup pfSense, Cloudflare, Pi-hole, and Twingate on the Edge of the network on separate hardware to the HomeLab servers to create a robust, secure, and efficient network environment. Below is the setup that achieves this:

### 1. **pfSense as the Primary Firewall and Router**

- **Role**: Act as the main firewall and router for your network.
- **Setup**:
  - **Interface Configuration**: Set up pfSense with DHCP and DNS.
  - **Dynamic DNS**: Use pfSense's Dynamic DNS feature to update your dynamic public IP with a DNS provider like Cloudflare, ensuring your domain (`kattenhorn.tech`) points to your home's IP.
  - **Port Forwarding/Reverse Proxy**: Configure NAT or use HAProxy (a package available in pfSense) to manage and secure access to home lab services.
  - **VPN Configuration**: You can optionally set up OpenVPN or wireguard on pfSense for secure access to your internal network.

### 2. **Cloudflare for DNS and Proxying**

- **Role**: Manage your domain's DNS records and optionally provide web traffic proxying for extra security.
- **Setup**:
  - **DNS Management**: Direct DNS requests for your services to your dynamic IP using Cloudflare's DNS service.
  - **Proxying**: Enable Cloudflare's proxy features (CDN, DDoS protection) for your public-facing services to add an extra layer of protection and anonymity.
  - **SSL/TLS**: Use Cloudflare's SSL/TLS features to ensure secure transactions. You can use full (strict) mode with certificates.

### 3. **Pi-hole for Network-wide Ad Blocking**

- **Role**: Serves as an ad blocker and additional DNS filtering solution for your network.
- **Setup**:
  - **DNS Configuration**: Set up devices and pfSense to use Pi-hole as the primary DNS server.
  - **Ad Blocking**: Customize blocklists to filter ads and malicious sites.
  - **Network Insight**: Gain visibility into DNS requests made by your devices.

### 4. **Twingate for Secure Remote Access**

- **Role**: Securely access internal services without exposing the network via port forwarding.
- **Setup**:
  - **Twingate Configuration**: Set up Twingate to facilitate secure remote access. Define resources that need access from outside the network. This way, sensitive internal services don't require direct internet exposure.

### 5. **NGINX Proxy Manager**

- Use alongside pfSense for managing reverse proxy configurations with a user-friendly interface.
- Facilitate SSL certificate management with automatic renewal (via Let's Encrypt).

### Network Diagram Scenario

- **[Internet]**
  - |
  - **[Cloudflare DNS and Proxy]**
  - |
  - **[pfSense]**
    - **Internal Network with DHCP and DNS**
    - **Dynamic DNS Updates**
    - **VPN/Remote Access Solutions**
  - **[Home Network]**
    - **Services [Pi-hole, NGINX Proxy Manager, etc.]**
    - **Twingate for Remote Access**
