# Mavlink-over-4G-LTE

Long range communication for drones is always a challenge. Most radios used for communication between drones and ground control stations (GCS) are single frequency radios offering very limited range and bandwith. Also the bandwidth falls drastically with distance increase, especially in urban areas. With 5G in pipeline and 4G LTE vailable, its a viable solution for getting mavlink with video feed between drones and GCS.

The challenge is use of internet for point to point commuication is the requirement of static IP or Dynamic DNS to route packets between drone and Ground Control Station. But a simpler solution to get started instantly is use cloud based VPN services such as openvpn to create your private network over internet. They allow upto three connections free of cost. 

Step 1 - Create your account on openvpn cloud services. Create three clients i.e drone, gcs and spare and download respective .ovpn files. The files have all the necessary information to connect to network. 

Step 2 - Install openvpn on companion computer and save its .ovpn file. Create a systemd script so that vpn service starts on boot automatically.

Step 3 - Install openvpn client on Ground Control Station (GCS) laptop or computer. In my case my laptop has Windows 10 and Mission Planner as GCS application. Use GCS .ovpn file to connect vpn on laptop.

Step 4 - Install mavproxy on companion computer and run the script with IP Address (VPN) of GCS for creating mavlink. Select udp pn GCS application at laptop to connect to companion computer on drone over internet. You can even take ssh access of companion computer and Flight Controller Unit (FCU) like Beagle Bone Blue which is Linux based.

Detailed steps with screenshots of each action will be uploaded soon !!!

