# Home Network Analyzer
![Version](https://img.shields.io/badge/Version-1.0.0-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey.svg)
![Price](https://img.shields.io/badge/Price-100%25%20Free-brightgreen.svg)

I built this tool because I got tired of digging through Windows menus just to flush my DNS, check my local ping, or remember an old Wi-Fi password. It's a straightforward diagnostic utility for Windows.

## What it actually does

*   **Network Scanner:** Pings your local IP range and checks ARP tables to see what devices are online.
*   **Wi-Fi Passwords:** Just runs a native Windows command to read the passwords you ALREADY saved on your PC. It is not a brute-force or hacking tool.
*   **Gaming Optimizer:** Modifies the Windows TCP/IP registry (specifically `TCPNoDelay` and `TcpAckFrequency`). Normally, Windows bundles packets together to save bandwidth. This forces Windows to stop buffering and send gaming packets instantly. It won't fix a bad ISP connection, but it removes artificial system latency.
*   **DNS Switcher:** Quickly swaps your network adapter's DNS to Cloudflare, Google, etc.
*   **Speedtest & iperf3:** Uses bundled `librespeed-cli` for internet speed testing and `iperf3` for testing your internal LAN capacity (router and cables).

## Why does it need Admin Rights?

Because Windows is strict. It will silently block any attempt to change DNS settings or tweak the TCP registry if you run the program as a normal user.

## Disclaimers & Credits

*   **Privacy:** This tool is completely local. It does not send logs, IP addresses, or Wi-Fi passwords to external servers. 
*   **Credits:** This project bundles `iperf3` (ESnet / BSD License) and `librespeed-cli` (GNU License). Full credit for the benchmarking engines goes to their respective open-source communities.
*   If you need tech support, want to report a bug, or just want to buy me a coffee, hit me up at: **adonis.ploae@yahoo.com**.
