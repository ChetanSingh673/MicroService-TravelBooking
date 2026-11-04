## Grafana Installation Guide via APT Repository
This guide walks you through installing Grafana on a Ubuntu Linux via APT Repository.

## 1. Add the Grafana APT key
```bash
sudo apt-get install -y software-properties-common wget
wget -q -O - https://apt.grafana.com/gpg.key | sudo gpg --dearmor -o /usr/share/keyrings/grafana.gpg
```
## 2. Add the Grafana repository
```bash
echo "deb [signed-by=/usr/share/keyrings/grafana.gpg] https://apt.grafana.com stable main" | sudo tee /etc/apt/sources.list.d/grafana.list
```
## 3. Update package list
```bash
sudo apt-get update
```
## 4. Install Grafana
```bash
sudo apt-get install -y grafana
```
## 5. Start and enable Grafana
```bash
sudo systemctl start grafana-server
sudo systemctl enable grafana-server
```
Grafana is now running as a systemd service and will auto-start on boot.

## 6. Access Grafana
Open your browser and visit:
```bash
http://localhost:3000
```
Default credentials:

Username: ```bash admin ```

Password: ```bash admin ``` (you'll be prompted to change it at first login)
