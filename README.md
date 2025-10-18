# Update system packages
sudo apt update && sudo apt upgrade -y

# Install required packages
sudo apt install -y curl wget git nginx certbot python3-certbot-nginx

# Install Node.js 18 (required version)
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs

# Verify installation
node -v
npm -v




# Clone the repository
git clone https://github.com/electromr/Hosting-panel.git
cd Hosting-panel

# Install project dependencies
npm install

# Make the project directory accessible
sudo chown -R $USER:$USER /path/to/Hosting-panel






# Edit the settings.json file
nano settings.json






# Start the panel application
node app.js

# Or use PM2 for production (recommended)
npm install -g pm2
pm2 start app.js --name "vizora-host"
pm2 startup
pm2 save
