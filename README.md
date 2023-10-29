----> Malware Detection in Network Traffic Data

This dataset offers detailed information to network malware researchers by including labels that describe the connections between flows associated with potentially malicious or damaging activities. At the Stratosphere laboratory, these labels were meticulously made using malware capture analysis.

There are 25000363 instances and 23 features in the given dataset.

----> Brief description about important columns - 

-ts: The timestamp of the connection event. (time)
-id.orig_p: The source port. (port)
-id.resp_p: The destination port. (port)
-proto: The network protocol used (e.g., 'tcp'). (enum)
-conn_state: The state of the connection. (string)
-history: A history of connection states. (string)
-label: A label associated with the connection (e.g., 'Malicious' or 'Benign'). (string)


----> Label Descriptions:

Attack: Signifies the occurrence of an attack originating from an infected device directed towards another host. This includes flows attempting to exploit vulnerable services, discerned through payload and behavioral analysis.

Benign: Denotes connections where no suspicious or malicious activities have been detected.

C&C (Command and Control): Indicates that the infected device has established a connection with a Command and Control server. This is rooted in the periodic nature of connections or activities such as binary downloads or the exchange of IRC-like or decoded commands.

DDoS (Distributed Denial of Service): Assigned when the infected device is actively involved in a Distributed Denial of Service attack, identifiable by the volume of flows directed towards a single IP address.

FileDownload: Signifies that a file is being downloaded to the infected device. Determined by examining connections with response bytes exceeding a specified threshold, often in conjunction with known suspicious destination ports or IPs associated with Command and Control servers.

HeartBeat: Designates connections where packets serve the purpose of tracking the infected host by the Command and Control server. Identified through response bytes below a certain threshold and exhibit periodic similarities.

Mirai: Applied when connections exhibit characteristics resembling those of the Mirai botnet, based on patterns consistent with common Mirai attack profiles.

Okiru: Similar to "Mirai," the "Okiru" label is assigned to connections displaying characteristics of the Okiru botnet. Parameters for this label are the same as for Mirai, but Okiru is a less prevalent botnet family.

PartOfAHorizontalPortScan: Employed when connections are involved in a horizontal port scan aimed at gathering information for potential subsequent attacks. The labeling decision hinges on patterns such as shared ports, similar transmitted byte counts, and multiple distinct destination IPs among the connections.

Torii: Used when connections exhibit traits indicative of the Torii botnet, with labeling criteria similar to those used for Mirai, albeit in the context of a less common botnet family.

----> Classification Problem:
We have performed classification problem on "Label" feature in order to predict to which class a particular malicious attack belongs to.
We have also performed classification problem on "protos" means protocols to predict which Network protocol is mostly attacked.


----> Work Distribution:
Every member in the group has worked individually on the dataset and the work can be seen in respective branches.

