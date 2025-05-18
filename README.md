# NetworkPLus-Domain5-TicketingLab
Documenting Simulation: User reports they can’t connect to the internet, but they’re working from home and can access local files. They aren’t sure if it’s the router or their computer.


# Issue Reported
User unable to connect to the internet while working reotely. Local apps work fine. User is unsure if it's a router or device issue.

# Initial Investigation
1. Asked user to confirm Wi-Fi/Network icon status
 > To verify if the system is physically connected or reporting a disconnect at the os level. 
2. Instructed user to run: 'ipconfig /all'
 > To check for an assigned IP address, default gateway, and DNS server. It helps detect DHCP issues or misconfigurations.
3. Reviewed DSN and gateway entries.
> Because mos internet access issues involve DNS misrouting or no gateway - also help confirms wether name resolution is failing or routing is broken.
4. Guided user to run: 'ping 8.8.8.8' and 'ping www.google.com'
>  Ping IP for Google DNS to raw internet access; and ping url to check if DNS is resolving hotsnames.
5. Used 'tracert' to verify routh path.
>  Helps visualize wherepackets are stopping; identifies whether the break is a the gateway, ISP level, orbeyond.

# Root Cause
- Default gateway was missing due to temporary loss of DHCP lease
- DNS unreachable until gateway was restored

# Resolution
- Had user renew IP; 'IPconfig /release' then 'ipconfig /renew'
- Importance of checking DNS and gateway together.
- Practiced clear step-by-step communication

# What to learn
- How to triage remote connectivity issues
- Importance of checking DNS and gateway together
- Practiced clear step-by-step communication

# Tools Used
- Command Prompt
- Ticket-style note format


## Related Domain
- Network+ Domain 5: Network Troubleshooting
