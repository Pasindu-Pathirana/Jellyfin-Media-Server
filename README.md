<h2><b>Jellyfin-Media-Server</b></h2>
<img width="1536" height="1024" alt="Logical Structure" src="https://github.com/user-attachments/assets/a8a3b940-1464-4170-b069-6071616716a1" />

<h3><b>Overview</b></h3>
This project demonstrates the deployment and configuration of a self-hosted media server using Jellyfin on Ubuntu Server. The system is configured for remote management via SSH and supports centralized media storage and streaming across a local network.

<h3><b>Objectives</b></h3>

   <li>  Deploy a media server using Jellyfin</li> 
   <li>  Configure secure remote access via SSH</li> 
   <li>  Manage file permissions for media access</li> 
   <li>  Enable client access over LAN</li> 
   <li>  Configure file sharing via Samba</li> 
   
<h3><b>Technologies used</b></h3>

   <li>  Ubuntu Server 22.04</li> 
   <li>  Jellyfin</li> 
   <li>  OpenSSH</li> 
   <li>  Samba </li> 
   <li>  Linux CLI</li> 

<h3><b>System Architecture</b></h3>
<img width="237" height="313" alt="image" src="https://github.com/user-attachments/assets/f10155d1-d1ed-4135-bc3e-e60f85680aad" />

<h3><b>Installation Steps</b></h3> (Ubuntu CLI)<br>
<br>
<b>1. Update System</b>
<br>

```bash
sudo apt update && sudo apt upgrade -y

```
<b>2. Install Jellyfin</b>

```bash
sudo apt install jellyfin

```
<b>3. Enable and Start Service</b>

```bash
sudo systemctl enable jellyfin
sudo systemctl start jellyfin

```

<b>4. Install SSH</b>

```bash
sudo apt install openssh-server

```

<h3><b>Access Jellyfin</b></h3>

```bash
http://<server-ip>:8096

```

<h3><b>Media Directory Setup</b></h3>

```bash
sudo mkdir -p /srv/media
sudo chown -R usr_name:usr_name /srv/media
sudo chmod -R 775 /srv/media

```

<h3><b>Permission Configuration</b></h3>

```bash
sudo usermod -aG media jellyfin

```

<h3><b>Samba Configuration</b></h3>

<b>Install :</b>

```bash
sudo apt install samba

```

<b>Edit :</b>

```bash
sudo nano /etc/samba/smb.conf

```

<b>Add :</b>

```bash
[Media]
path = /srv/media
browseable = yes
read only = no

```

<b>Restatrt :</b>

```bash
sudo systemctl restart smbd

```

<h3><b>✅ Testing & Verification</b></h3>

   <li>  Jellyfin web UI accessible</li> 
   <li>  Media files detected</li> 
   <li>  Streaming works on client</li> 
   <li>  SSH remote login successful </li> 

<br>

<h3><b>Screenshots</b></h3>

 




   
   
