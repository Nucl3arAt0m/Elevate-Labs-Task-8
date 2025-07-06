# VPN Setup and Testing Report - Elevate Labs Task 10

## Task Overview
- **Objective**: Set up and test a free VPN client for Day 10 of the Elevate Labs Cybersecurity Internship (July 4, 2025).
- **Tool Used**: ProtonVPN free tier on Ubuntu.
- **Goal**: Configure VPN, verify IP change, confirm encryption, and summarize benefits/limitations.

## Setup and Testing Process

1. **Signed Up for ProtonVPN**:
   - Visited [protonvpn.com](https://protonvpn.com), created a free account with email.
   - Verified email to activate account.

2. **Installed ProtonVPN Client**:
   - Downloaded `.deb` package:
     ```bash
     cd ~/Downloads
     wget https://protonvpn.com/download/protonvpn-stable-release_1.0.3-2_all.debwget https://repo.protonvpn.com/debian/dists/stable/main/binary-all/protonvpn-stable-release_1.0.8_all.deb
     ```
   - Installed dependencies and client:
     ```bash
     sudo dpkg -i ./protonvpn-stable-release_1.0.8_all.deb && sudo apt update
     ```

3. **Connected to VPN Server**:
   - Launched client: `protonvpn-app`
   - Logged in, selected Netherlands server.
   - Connected successfully.
   - Screenshot: `Screenshots/protonVPN.png`

4. **Verified IP Address Change**:
   - Pre-VPN: Visited [whatismyipaddress.com](https://whatismyipaddress.com), noted original IP.
   - Screenshot: `Screenshot/current_ipAddr.png`
   - Post-VPN: Connected to Netherlands server, refreshed page, confirmed new IP (Netherlands-based).
   - Screenshot: `Screenshots/ipAddr_with_VPN.png`

5. **Confirmed Encrypted Browsing**:
   - Browsed `google.com` with VPN on, traffic encrypted via AES-256.
   - Verified no data leaks (ISP cannot see browsing activity).

6. **Disconnected VPN and Compared**:
   - Disconnected via ProtonVPN app.
   - Revisited [whatismyipaddress.com], confirmed original IP returned.

## VPN Encryption and Privacy Features
- **Encryption**:
  - **AES-256**: Uncrackable, industry-standard encryption.
  - **Protocols**: WireGuard (fast, secure), OpenVPN (robust, audited).
- **Privacy Features**:
  - **No-Logs Policy**: No browsing history or connection logs stored, audited by third parties.[](https://www.pcmag.com/picks/the-best-free-vpns)
  - **Kill Switch**: Blocks traffic if VPN disconnects, preventing IP leaks.
  - **NetShield**: Blocks ads/trackers (limited in free tier).
  - **IP Masking**: Hides real IP, preventing ISP tracking.
- **Source**: [ProtonVPN features](https://protonvpn.com)[](https://protonvpn.com/features)

## VPN Benefits and Limitations
- **Benefits**:
  - **Privacy**: Masks IP, prevents ISP tracking.
  - **Security**: Encrypts traffic, safe on public Wi-Fi.
  - **Censorship Bypass**: Access restricted content.
  - **Free Tier**: Unlimited data, no ads, strong privacy.[](https://protonvpn.com/free-vpn)
- **Limitations**:
  - **Speed**: Free servers may be slower due to load.[](https://windscribe.com/blog/windscribe-vs-protonvpn/)
  - **Servers**: Limited to 5 countries (Netherlands, Japan, Poland, Romania, US).
  - **Streaming**: No access to streaming-optimized servers.
  - **Single Device**: One connection at a time.[](https://www.pcmag.com/picks/the-best-free-vpns)

## Learnings
- **VPN Utility**: Enhances privacy and security via encryption and IP masking.
- **Trade-offs**: Free tiers balance cost with limited features/speed.
- **Next Steps**: Explore advanced features like Secure Core or paid plans for streaming.

## Files Included
- `Screenshots/current_ipAddr.png`: VPN connection status.
- `Screenshots/ipAddr_with_VPN.png`: VPN IP verification.
- `vpn_setup_report.md`: This report.
- `README.md`: Task overview.
- `notes.md`: Setup steps.

## Portfolio
This task is part of my Elevate Labs internship portfolio: [Elevate-Labs-Internship-Tasks](https://github.com/Nucl3arAt0m/Elevate-Labs-Internship-Tasks).
