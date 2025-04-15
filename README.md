# VDRPSDP-MC-Dataset

README - Dataset for ALNS-DQN in Humanitarian Logistics

This repository contains the benchmark instances used in the paper titled:
"Multi-Commodity Vehicle-drone Routing Problem with Simultaneous Delivery and Pickup in Humanitarian Logistics"

📁 Contents:
-------------
- /instances/:
  Contains all instance files used in the numerical experiments (e.g., 5_0.1_1.txt).
  Each file name follows the format: [number of affected areas]_[lambda value]_[index].txt

📄 Instance File Format:
------------------------
Each instance file includes:
1. Header with truck capacity, drone capacity, and lambda:
   truckCAPACITY	droneCAPACITY	lambda

2. A list of affected areas including the depot:
   Format:
   NO.  XCOORD.  YCOORD.  D1  D2  D3  P1  P2  P3  DEADLINE

   - NO.: Node ID (0 = depot)
   - XCOORD., YCOORD.: Coordinates of each node
   - D1~D3: Delivery demands for commodity types 1–3
   - P1~P3: Pickup demands for commodity types 1–3
   - DEADLINE: Maximum allowable delivery time for each node

Example:
---------
1	1	12	14	0	13	0	27	0	45
2	10	7	12	0	0	0	16	17	259
... (node list continues)

🔍 Notes:
----------
- Units for delivery and pickup quantities are consistent across all commodities.
- **Lambda (λ)** denotes the proportion of affected nodes that are **inaccessible to vehicles** and **must be served by drones only**.
📌 Citation:
-------------
If you use these instances, please cite our paper accordingly.

📬 Contact:
------------
For questions, feel free to contact: [pwh@stu.scu.edu.cn]
