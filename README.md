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

```bash
sudo apt update && sudo apt upgrade -y
