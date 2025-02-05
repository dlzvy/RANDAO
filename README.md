# RANDAO

## Steps

### 1. Install docker 
```bash
sudo apt install docker.io
```
```bash
sudo apt install docker-compose
```
```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin -y
```
### 1. Clone Repository

```bash
git clone https://github.com/RandAOLabs/Randomness-Provider.git
``` 
```bash
cd Randomness-Provider
```
```bash
cd docker-compose
```
### 2. Deploy Node 
```bash
cp .env.example .env
``` 
### 3. Ganti file .env
```bash
nano .env
```
### 4. Edit 
```
provider_id: Your unique provider identifier
local_db_user: Database username
local_db_password: Database password
local_wallet_json: Wallet JSON (either direct or via file)

PROVIDER_ID = wallet Address
wallet json = private key     

Export the private key from the wallet and open it in a plain text editor such as Notepad.‍
The private key you extract is in a JSON file format. Load it into the .env file as shown in the example by using the nano .env command, and make sure it matches the structure provided.
``` 
### 4. Pull dan run 
```bash
docker pull randao/vdf_job:v0.1.4
```
```bash
docker-compose up -d
```
### 5. Check Logs
```bash
docker-compose logs -f
```

### 6. Optional command for shutdown docker and restart docker
```bash 
docker-compose down
```
```bash 
docker restart CONTAINER_NAME
```




