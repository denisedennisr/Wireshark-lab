<h1>Capture Packet with Wireshark</h1>


<h2>Description</h2>
In this scenario, I am a security analyst investigating traffic to a website.
Throughout this lab I use Wireshark to inspect packet data and apply filters to sort through packet information efficiently. I’ll analyze a network packet capture file that contains traffic data related to a user connecting to an internet site. I'll apply data filters in order to identify the source and destination IP addresses involved in this web browsing session, examine the protocols that are used when the user makes the connection to the website, and analyze some of the data packets to identify the type of information sent and received by the systems that connect to each other when the network data is captured.
<br />
<h2>Explore data with Wireshark</h2>
In this task, I have to open a network packet capture file that contains data captured from a system making web requests to a site. I will use Wireshark to open this data and gain a better understanding of how it is presented within the application.
<img src="https://imgur.com/w3mefRL.png" height="80%" width="80%" alt="Wireshark pcap"/>

<h2>Apply a basic Wireshark filter and inspect a packet</h2>
In this task, I opened a packet in Wireshark for more detailed exploration and filtered the data to inspect the network layers and protocols contained in the packet.
<br>
<br>
<img src="https://imgur.com/kYmu7Rr.png" height="80%" width="80%" alt="Wireshark pcap"/>
<br />
<br />
The list of packets displayed is now significantly reduced and contains only packets where either the source or the destination IP address matches the address I entered. Now only two packet colors are used: light pink for ICMP protocol packets and light green for TCP (and HTTP, which is a subset of TCP) packets.

<h2>Use filters to select packets</h2>
In this task, I will utilize filters to examine particular network packets, considering their origin or destination. I will delve into the selection of packets based on either their physical Ethernet Media Access Control (MAC) address or their Internet Protocol (IP) address.
<h2>Filter to select traffic for a specific source IP address only</h2>
<br>
<br>
<img src="https://imgur.com/jA5EIdr.png" height="80%" width="80%" alt="Wireshark pcap"/>
A filtered list is returned, it contains only packets that came from 142.250.1.139.
<br />
<br />
<h2>Filter to select traffic for a specific destination IP address only</h2>
<img src="https://imgur.com/wP4sD9X.png" height="80%" width="80%" alt="Wireshark pcap"/>
<br />
<br />
A filtered list is returned that contains only packets that were sent to 142.250.1.139.  <br/>
<h2>  Use filters to explore DNS packets</h2>
In this task, i will use filters to select and examine DNS traffic. Once I've selected sample DNS traffic, I’ll drill down into the protocol to examine how the DNS packet data contains both queries (names of internet sites that are being looked up) and answers (IP addresses that are being sent back by a DNS server when a name is successfully resolved).
<img src="https://imgur.com/nc3V4T6.png" height="80%" width="80%" alt="Wireshark pcap"/>
<br />
<br />
You’ll notice that the name of the website that was queried is opensource.google.com.  <br/>
<img src="https://imgur.com/jhWA3KR.png" height="80%" width="80%" alt="Wireshark pcap"/>
<br />
<br />
The Answers data includes the name that was queried (opensource.google.com) and the addresses that are associated with that name. <br/>

<h2> Use filters to explore TCP packets</h2>
In this task, I’ll use additional filters to select and examine TCP packets. I’ll search for text that is present in payload data contained inside network packets. This will locate packets based on something such as a name or some other text.

<img src="https://imgur.com/dIfiSuF.png" height="80%" width="80%" alt=" Wireshark pcap"/>
<br />
<br />
Observe that this filters to packets containing web requests made with the curl command in this sample packet capture file.  <br/>
<h2> Summary </h2>
In this lab I utilized wireshark to open saved packet capture files, view general packet data and apply filters to examine specific packet details.

