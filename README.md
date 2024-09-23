
### Step 1: Configure accounts
Create a `data.txt` file in the root directory.
Add Telegram authentication data for each account on a new line:

1. Use PC/Laptop or Use USB Debugging Phone
2. open the `real goats bot`
3. Inspect Element `(F12)` on the keyboard
4. at the top of the choose "`Application`" 
5. then select "`Session Storage`" 
6. Select the links "`dev.goatsbot.xyz`" and "`tgWebAppData`"
7. Take the value part of "`tgWebAppData`"
8. take the part that looks like this: 

```txt 
query_id=xxxxxxxxx-1
query_id=xxxxxxxxx-2
query_id=xxxxxxxxx-3
```
9. Decode query_id= with https://www.urldecoder.org/
10. add it to `data.txt` file or create it if you dont have one

### Step 2: Modify Configurations (Optional)
The `config.json` file allows you to modify script settings:
account_delay: Time (in seconds) between account operations.
looping: Time (in seconds) before starting a new loop of account runs.

### Configuration
You can adjust the bot's behavior via config.json:

```json
{
    "use_proxies": false,
    "account_delay": 5,
    "looping": 3800
  }  
```
`account_delay`: Delay in seconds between switching accounts.
`looping`: Time in seconds to wait before running all accounts again.

### Format of proxies.txt
The proxies.txt file should contain one proxy per line in the following format:

```ruby
username:password@ip:port
username:password@ip:port
```

### Step 3: Run the script
To start the bot, run:

```bash
python main.py
```

### Additional Information
`The script` uses asyncio for asynchronous operations to handle multiple tasks concurrently.
`Error handling` is implemented to gracefully manage login and mission completion failures.
Proxy Format The proxies should be listed in a `proxies.txt` file with the format `username:password@ip:port`, one proxy per line.
Random Proxy Assignment The script will assign a proxy from the list for each account.