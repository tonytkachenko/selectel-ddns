# selectel-ddns

Selectel DDNS.
The script updates domain records using Selectel API. It takes the server's public IP and sets it to the chosen domains.

## Requirements

* Linux
* curl

## Installation

0. Clone repo
1. Rename `.env.sample` to `.env`
2. Set variables in the `.env` file.
3. Run `chmod +x shdotenv`

Now you can call `selectel-ddns` from terminal or setup a cron job.
