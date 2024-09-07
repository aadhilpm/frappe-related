Add Swap Memory in Ubuntu 24

# Check current swap
free -h

# Create a 2GB swap file (you can increase this size if needed)
sudo fallocate -l 2G /swapfile

# Set permissions for the swap file
sudo chmod 600 /swapfile

# Format the file as swap
sudo mkswap /swapfile

# Enable the swap file
sudo swapon /swapfile

# Check current swap
free -h
