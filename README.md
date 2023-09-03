# Idle-Recon
"Idle Recon" automates various reconnaissance tasks for bug bounty hunting or security testing purposes. It provides several functions that can be selected by the user:

- **Recon**: This function performs recon on a specified domain. It creates a directory for the domain, executes different tools such as `subfinder`, `assetfinder`, `ctfr`, `amass`, and `ffuf` to gather subdomains, and then processes and filters the obtained subdomains.

- **Scraping subdomains from all bug bounty programs**: This function downloads a `wildcards.txt` file from a repo that contains all the wildcards of all the publicly available bug bounty programs, removes asterisks (*) at the beginning of each line, and enumerates subdomains for each domain in the modified file. It combines the results and saves them in a subdomains.txt file.

- **JS scraping**: This function collects JavaScript (JS) files from the live subdomains obtained in the previous steps. It uses the tools `subjs`, `waybackurls`, and `httpx` to collect and process the JS files, saving the results in a js.txt file.

- **Subdomain Takeover**: This function checks for potential subdomain takeover vulnerabilities. It uses the tool `subzy` to scan the subdomains obtained earlier and saves the results in a `subzy.txt` file.

- **Resolving IPs from subdomains**: This function resolves the IP addresses of the live subdomains. It uses the tool `massdns` with a list of DNS resolvers to perform DNS lookups and saves the results in a resolved.txt file.

- **URL scraping**: This function scrapes URLs from a specified domain. It uses the tools `waybackurls`, `gau`, `hakrawler`, and `httpx` to collect and filter live URLs, saving the results in a `live_urls.txt` file.
<br><br><br>

## To use this tool, you can follow these steps:
- Download the script and save it as a Bash (.sh) file.
- Open the script in a text editor.
- Modify the tool directories according to your needs. For example, update the paths for `subfinder`, `assetfinder`, `ctfr`, `amass`, `ffuf`, `subjs`, `waybackurls`, `gau`, `hakrawler`, `httpx`, `subzy`, and `massdns` to match the locations where you have installed these tools on your system.
- Save the modified script.
- Make the script executable by running the command: `chmod +x idle.sh`.
- Run the script by executing: `./idle.sh`.
- Follow the on-screen prompts to select and execute the desired function.

Please note that this script assumes you have the required tools installed on your system and have set up the necessary dependencies. Make sure to update the tool paths and install any missing dependencies before running the script.

### License:
Idle-recon is an open-source tool released under the [MIT License.](/LICENSE)
