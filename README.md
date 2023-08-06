# Analyzing-Network-Secuirty
A fake scenario where a cybersecurity analyst is tasked with determining which network protocol was affected during a cyber incident using tools such as tcpdump and an ICMP

Review the scenario below. Then complete the step-by-step instructions.

You are a cybersecurity analyst working at a company that specializes in providing IT consultant services. Several customers contacted your company to report that they were not able to access the company website www.yummyrecipesforme.com, and saw the error “destination port unreachable” after waiting for the page to load. 

You are tasked with analyzing the situation and determining which network protocol was affected during this incident. To start, you visit the website and you also receive the error “destination port unreachable.” Next, you load your network analyzer tool, tcpdump, and load the webpage again. This time, you receive a lot of packets in your network analyzer. The analyzer shows that when you send UDP packets and receive an ICMP response returned to your host, the results contain an error message: “udp port 53 unreachable.” 

In the DNS and ICMP log, you find the following information:

In the first two lines of the log file, you see the initial outgoing request from your computer to the DNS server requesting the IP address of yummyrecipesforme.com. This request is sent in a UDP packet.

Next you find timestamps that indicate when the event happened. In the log, this is the first sequence of numbers displayed. For example: 13:24:32.192571. This displays the time 1:24 p.m., 32.192571 seconds.

The source and destination IP address is next. In the error log, this information is displayed as: 192.51.100.15.52444 > 203.0.113.2.domain. The IP address to the left of the greater than (>) symbol is the source address. In this example, the source is your computer’s IP address. The IP address to the right of the greater than (>) symbol is the destination IP address. In this case, it is the IP address for the DNS server: 203.0.113.2.domain

The second and third lines of the log show the response to your initial ICMP request packet. In this case, the ICMP 203.0.113.2 line is the start of the error message indicating that the ICMP packet was undeliverable to the port of the DNS server.

Next are the protocol and port number, which displays which protocol was used to handle communications and which port it was delivered to. In the error log, this appears as: udp port 53 unreachable. This means that the UDP protocol was used to request a domain name resolution using the address of the DNS server over port 53. Port 53, which aligns to the .domain extension in 203.0.113.2.domain, is a well-known port for DNS service. The word “unreachable” in the message indicates the message did not go through to the DNS server. Your browser was not able to obtain the IP address for yummyrecipesforme.com, which it needs to access the website because no service was listening on the receiving DNS port as indicated by the ICMP error message “udp port 53 unreachable.”

The remaining lines in the log indicate that ICMP packets were sent two more times, but the same delivery error was received both times. 

Now that you have captured data packets using a network analyzer tool, it is your job to identify which network protocol and service were impacted by this incident. Then, you will need to write a follow-up report. 

As an analyst, you can inspect network traffic and network data to determine what is causing network-related issues during cybersecurity incidents. Later in this course, you will demonstrate how to manage and resolve incidents. For now, you only need to analyze the situation. 

This incident, in the meantime, is being handled by security engineers after you and other analysts have reported the issue to your direct supervisor. 

	Step 1: accessing cyber security incdient response templete 

insert templete download here

	Step 2: accessing supporting documents 
insert dns and icmp traiffic log 
	Step 3: Provide a summary of the problem found in the DNS and ICMP traffic log
The network traffic analyzer tool inspects all IP packets traveling through the network interfaces of the machine it runs on. Network packets are recorded into a file. After analyzing the data presented to you from the DNS and ICMP traffic log, identify trends in the data. Assess which protocol is producing the error message when resolving the URL with the DNS server for the yummyrecipesforme.com website. Recall that one of the ports that is displayed repeatedly is port 53, commonly used for DNS. In your analysis:  

Include a brief summary of the DNS and ICMP log analysis and identify which protocol was used for the ICMP traffic.

Provide a few details about what was indicated in the logs.

Interpret the issues found in the logs.

Record your responses in part one of the cybersecurity incident report.  

	Step 4: Explain your analysis of the data and provide one solution to implement 
Now that you’ve inspected the traffic log and identified trends in the traffic, describe why the error messages appeared on the log. Use your answer in the previous step and the scenario to identify the reason behind the ICMP error messages. The error messages indicate that there is an issue with a specific port. What do the different protocols involved in the log reveal about the incident? In your response:

State when the problem was first reported.

Provide the scenario, events, and symptoms identified when the event was first reported.  

Describe the information discovered while investigating the issue up to this point.

Explain the current status of the issue.

Provide the suspected root cause of the problem.

List the next steps needed to troubleshoot and resolve the issue.

Record your responses in part two of the cybersecurity incident repo
