
# Local Network Port Scan Report (Redacted)

## Objective
This task aimed to identify open ports on devices within the local network and assess potential security exposure. For privacy, all IP addresses and hostnames have been redacted.

## Tools Used
- **Nmap** 
- **Wireshark** (for packet capture; raw `.pcap` files not included)  
- **Operating System:** macOS 

## Scan Details
The following command was used to perform the scan:

```bash
sudo nmap -sS -Pn -oX scan_results.xml x.x.x.x/24
````

Outputs were processed and redacted for privacy:

* `nmap_scan_results_redacted.txt`
* `scan_results_redacted.html`

## Key Findings

* **Number of hosts detected:** 3
* **Notable open ports (redacted):**

  * **Host A (`x.x.x.x`)**: 80, 443, 1900, 8080, 8443
  * **Host B (`x.x.x.x`)**: 5000, 7000
  * **Host C (`x.x.x.x`)**: 2869

## Risks & Recommendations

* **UPnP:** Disable if not required, as it can expose devices to external attacks.
* **Admin Interfaces:** Restrict access, enforce HTTPS, and use strong passwords.
* **Firmware:** Keep all network devices up to date to patch known vulnerabilities.
* **Network Segmentation:** Apply firewall rules to block unnecessary ports and isolate guest networks from the main network.

## Artifacts Included

* `scan_results_redacted.html` — redacted Nmap report
* `nmap_scan_results_redacted.txt` — redacted textual output
* `screenshots/` — screenshots showing packet flows and Nmap results
* `pcap_summary_redacted.txt` — summary of captured network packets (if included)

