# Selectel DNS Updater

This is a Bash script for updating the A records of domains and subdomains on Selectel DNS. It compares the current public IP address of the machine running the script to the IP address in the DNS record and updates the DNS record if necessary.

## Requirements

* Bash shell
* cURL command-line tool
* JQ command-line tool
* Selectel API token with the appropriate permissions

## Installation

1. Clone the repository or download the script file.
2. Install the required packages.

    On Ubuntu or other Debian-based Linux distributions, you can install these packages using the following command:

    ```bash
    sudo apt-get install jq curl
    ```

    If you are using a different Linux distribution, you may need to use a different package manager or installation method.

3. Rename `.env.sample` file to `.env`. Replace `<your token here>` with your Selectel API token, `<main domain>` with your root domain and `<domains to update>` with a space-separated list of domains and subdomains to update.

4. Make the shell script executable by running the following command:

    ```bash
    chmod +x selectel-ddns
    ```

## Usage

Run the script using the following command:

```bash
./selectel-ddns
```

The script will update the A record of each domain or subdomain in the list if the current IP address differs from the current external IP address.

## Troubleshooting

* If you encounter errors while running the script, check that all required dependencies are installed and that the `.env` file is present and contains valid values.
* If you receive error messages from the Selectel API, double-check your API token.
