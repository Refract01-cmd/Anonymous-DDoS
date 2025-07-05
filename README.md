# Anonymous-DDoS

---

## About

**Anonymous-DDoS** is a powerful and versatile DDoS tool designed to test the resilience of network infrastructure. It features multiple attack methods and advanced bypass techniques to simulate various types of network stress.

**Please Note:** This software is **proprietary (closed-source)** and is distributed in an encrypted/compiled format. Its source code is not publicly available for review, modification, or redistribution.

## Features

* **HTTP Flood:** Generates high volumes of HTTP requests with intelligent header randomization to bypass bot detection.
* **Cloudflare Bypass:** Utilizes `cloudscraper` to navigate Cloudflare's JavaScript challenges.
* **Smart Proxy Management:** Integrates with proxy lists (e.g., `proxies.txt`), automatically handling proxy health checks and retries for efficient attack execution.
* **Tor Support:** Option to route traffic through the Tor network for enhanced anonymity.
* **Multi-threaded:** Capable of launching attacks with multiple concurrent threads for increased impact.
* **Diverse Attack Methods:**
    * **Slowloris:** Keeps connections open to exhaust server resources.
    * **UDP Flood:** Floods targets with UDP packets.
    * **TCP Flood:** Initiates and closes numerous TCP connections.
    * **DNS Flood:** Overwhelms DNS servers with excessive domain resolution requests.
    * **TLS Handshake Flood:** Bombards HTTPS servers with resource-intensive TLS handshakes.

---

## Usage

### Prerequisites

* Python 3.x
* Required Python libraries (install via `pip install -r requirements.txt`)

### Installation

1.  Clone this repository (or download the compiled version):
    ```bash
    git clone https://github.com/Refract01-cmd/Anonymous-DDoS.git
    cd Anonymous-DDoS
    ```
2.  Install the necessary Python packages:
    ```bash
    pip install -r requirements.txt
    ```

### Proxy List (`proxies.txt`)

If you plan to use proxies, ensure you have a `proxies.txt` file in the root directory with one proxy per line in `IP:PORT` format.

**Example `proxies.txt`:**


192.168.1.1:8080
1.2.3.4:3128

### Running the Tool

```bash
python main.py --help

Here are some common usage examples:
 * HTTP Flood with Cloudflare Bypass:
   python main.py --url [https://example.com](https://example.com) --method http --threads 100 --bypass cloudflare

 * HTTP Flood with Proxies:
   python main.py --url [https://example.com](https://example.com) --method http --threads 150 --proxy proxies.txt

 * DNS Flood (targeting egitici.site's authoritative nameserver for 5 minutes):
   python main.py --url egitici.site --method dns --threads 50 --time 300 --dns-server 67.207.67.2

 * Slowloris Attack:
   python main.py --url [https://example.com](https://example.com) --method slowloris --threads 10 --time 600

Important Legal Notice
This software is proprietary and protected by copyright.
 * The source code is encrypted and not available for public inspection or modification.
 * You are strictly prohibited from decompiling, reverse-engineering, disassembling, modifying, creating derivative works from, or in any way attempting to analyze the underlying functionality or source code of this software.
 * Any unauthorized distribution, sharing, or publication of modified versions, derivative works, or the decrypted source code of this software on public repositories (e.g., GitHub) or any other platform is strictly forbidden.
 * By using this software, you agree to these terms.
For full terms and conditions, please refer to the LICENSE.txt file in this repository.
Disclaimer
This tool is intended for ethical testing purposes only, with explicit permission from the target system owner. Unauthorized use against any network or system is illegal and strictly forbidden. The developer assumes no liability for any misuse or damage caused by this software.
