
## Honeypot Project
A Cowrie SSH honeypot project on Kali Linux.
---

## 1. Clone This Repository

```
git clone https://github.com/Arinah-Tech/honeypot-project.git
cd honeypot-project
```

---

## 2. Install Dependencies

```
sudo apt update
sudo apt install git python3-venv python3-pip libssl-dev libffi-dev build-essential -y
```

---

## 3. Install and Configure Cowrie

```
git clone https://github.com/cowrie/cowrie.git
cd cowrie
python3 -m venv cowrie-env
source cowrie-env/bin/activate
pip install --upgrade pip setuptools wheel
pip install -r requirements.txt
pip install twisted[conch] cryptography service_identity pyopenssl
cp etc/cowrie.cfg.dist etc/cowrie.cfg
```
---

## Running the Honeypot
**Start Cowrie:**

```
bin/cowrie start
```

**Check status:**

```
bin/cowrie status
```
**Run in debug mode:**

```
bin/cowrie debug
```
---

## Testing
Connect locally to the honeypot (default port 2222):

```
ssh root@127.0.0.1 -p 2222
```
