# Process-Analytics-Case-Studies---Simulation-Project---Extend-sim

Questions

9.8.5 Case 5: Performance Analysis and Improvement of an Internet Ordering Process
The management of a software company wants to study the performance of the company’s web order processing. The interarrival times of orders are exponentially distributed with a mean of 7 minutes. Orders are placed through the company’s webpage, using an electronic ordering form, or via e-mail. On arrival, a clerk looks for the buyer’s name in the compa- ny’s database. The time required to look for a name in the database is uniformly distributed between 20 and 45 seconds. If the buyer is not in the database, the clerk enters the buyer’s information, which includes name, address, phone number, and e-mail address. The time required to enter the buyer’s information in the database is uniformly distributed between 10 and 30 seconds. Approximately 60 percent of the time, the buyer ’s name is not in the database.
Some orders are for an upgrade of the software, and the others are from first-time buyers. For all practical purposes, it takes no time to figure out whether an order is for an upgrade or from a first-time buyer. Approximately 30 percent of the orders are for upgrades. If the order is for an upgrade, then the clerk simply enters a code in the electronic purchase order (PO), created when the buyer’s name was entered or found in the database. (This code is later e-mailed to the customer, so he or she can download an upgrade from the company’s website.) Entering the code requires an exponentially distributed time with a mean of 2 minutes, because the clerk needs to verify the customer’s current software version and platform. Once the code is entered, the electronic PO goes to accounting.
When the order is from a first-time buyer, the clerk checks whether the buyer wants the CD version with printed documentation or whether he or she prefers to download the software from the company’s website. This requires an exponentially distributed time with a mean of 1 minute, because sometimes, this information has been misplaced. About 70 percent of the buyers prefer the CD version. When the CD version is preferred, the clerk needs to retrieve it from the storage room. This activity requires a normally distributed time with a mean of 5 minutes and a standard deviation of 1 minute. The clerk then pre- pares the software for shipping, which takes between 3 and 6 minutes (uniform distribu- tion). If the buyer prefers to download the software, the clerk enters an appropriate code in the electronic PO. Entering the code requires an exponentially distributed time with a mean of 1 minute, because a computer program sometimes is slow at generating a license for each customer.
Purchase orders for upgrades and first-time buyers go to accounting after a clerk has either entered a code for downloading or prepared the CD version for shipping. Accounting personnel charge the purchase to a credit card (exponential distribution with a mean of 2 minutes) and prepare the invoice. Data on invoice preparation times has been collected and is available in Table 9.20. Finally, the accounting personnel mail the software or e-mail the access code with the invoice. This activity requires a uniformly distributed time between 45 and 90 seconds.

TABLE 9.20
Observed Invoice Preparation Times in Minutes
No. Invoice No. Invoice No. Invoice No.
Invoice Preparation
0.721 1.132 0.705 1.211 0.831 0.866 1.243 0.431 1.193 1.193 1.220 0.954 1.050 0.747 1.270 0.754 0.807 0.890 0.771 1.099 1.114 0.982 1.235 1.152 0.708 0.745 0.938 1.384 1.033 1.378
 Preparation
1 0.987 31
2 0.881 32
3 1.022 33
4 0.799 34
5 0.986 35
6 1.053 36
7 0.493 37
8 0.883 38
9 1.028 39
10 1.057 40
11 0.793 41
12 1.068 42
13 0.836 43
14 0.984 44
15 1.092 45
16 1.006 46
17 1.113 47
18 0.914 48
19 0.877 49
20 1.196 50
21 1.139 51
22 0.937 52
23 0.640 53
24 1.347 54
25 0.961 55
26 1.004 56
27 1.068 57
28 1.170 58
29 1.406 59
30 1.288 60
Preparation
1.037 61 1.103 62 0.965 63 1.199 64 0.989 65 1.055 66 0.916 67 0.611 68 1.044 69 0.775 70 0.975 71 0.699 72 0.948 73 1.072 74 0.929 75 0.752 76 1.041 77 0.878 78 1.180 79 1.326 80 1.064 81 0.803 82 1.035 83 1.073 84 1.011 85 1.300 86 1.333 87 1.043 88 0.810 89 1.141 90
Preparation
0.875 91 0.763 92 1.283 93 0.856 94 1.091 95 1.028 96 1.163 97 0.972 98 1.082 99 0.578 100 0.717 101 1.473 102 1.418 103 1.119 104 1.102 105 1.208 106 0.970 107 0.757 108 1.189 109 1.183 110 1.300 111 1.280 112 1.023 113 0.852 114 1.148 115 0.972 116 0.747 117 1.031 118 1.190 119 1.017 120
  Currently, the company employs two people for this process: one clerk for the initial pro- cessing and one person in charge of the accounting. However, management is considering adding one person to the process and would like to use simulation to determine where to add this new employee to obtain the maximum customer service benefit.
9.8.5.1 Questions
1. The first task is to understand this process, so you should develop a flowchart. This chart should be the first exhibit in your written report.
2. Using the flowchart as a guideline, develop a simulation model of this process. To build a valid model, the available data on how long it takes to prepare an invoice
Input and Output Data Analysis 419
needs to be analyzed. More precisely, a suitable distribution should be fitted to the data. Because only two resource types are in this process (the clerks and the accounting personnel), your model should have only two queues.
3. Set the random seed value to 34 in the Simulation Setup of the Run menu. Run the model for 15 working days and collect the waiting time at the queues, cycle time, resource use, and WIP. (A working day consists of 8 hours.)
4. Discuss the performance of the current process based on the collected data. Include the following exhibits to support your arguments: queue statistics, line graphs of resource use, a histogram of cycle times, and the WIP value at the end of the 15 days.
5. Identify the bottleneck, and add the new employee to the bottleneck. Compare the use of clerks and accounting personnel before and after adding the new employee. Also compare the frequency distribution of cycle times before and after adding the new employee. Include line graphs for the use of resources after adding the new employee and a histogram of cycle times.




10A.2 Emergency Room Staffing*
An emergency department (ED) is open 24 hours a day and receives an average of 145 patients daily. Besides its internal capacity, the ED shares resources with other hospital services, such as X-rays, scanners, clinical laboratories, and pharmacy. Patients arriving at the ED follow a process as depicted in Figure 10.14. The process begins when a patient arrives through the doors of the ED and ends when a patient is either released from the ED or admitted into the hospital for further treatment. There are two types of arrivals: walk-in patients, who are required to see a receptionist, and ambulance patients, who bypass the receptionist and enter the examination room directly. The acuity of the patient’s illness is assessed by a doctor in the examination room. Also in the examination room, doctors will decide whether the patient needs further tests, such as X-rays and clinical lab tests, performed by a patient care lab technician. Patients are classified as critical (Category 1) or noncritical according to their condition. After an assessment has been performed by the doctor, the noncritical patients are further classified into two categories. Category 2 patients are asked to wait for a minor treatment, which is performed by a nurse in the treatment room. Category 3 patients receive their medication and are released from the hospital. Each critical patient is assigned to a bed in the emergency room, where he/ she receives complete treatment and stays under close observation. The treatment services in the emergency room are provided by a nurse and a doctor; the doctor is called from the examination room when needed. Finally, critical patients are either released or admitted into the hospital for further treatment. Patients who arrive at the hospital in an ambulance are considered critical patients (Category 1) and are rushed immediately to the emergency room. It is observed that 88 percent of all patients are released from the emergency room, while the remaining 12 percent are admitted into the hospital for further treatment. The ED has the following resources:
• Receptionists
• Doctors
• Lab technicians
• Treatment room nurses
• Emergency room nurses
Due to layout considerations, hospital administrators have determined that the staffing level must not exceed three receptionists, six doctors, three lab technicians, three treat- ment room nurses, and eight emergency room nurses. The hospital would like to find the configuration of resources that maximizes patient throughput (patients dismissed per unit of time) subject to budget constraint and a constraint imposed on the average waiting time in the system for patients of Category 1.
A comprehensive survey has been carried out at the ED to collect data on the arrival pro- cess, the service times at the examination room, the service times at the treatment room, and the total turnaround time in the ED. After observing the process for 3 weeks and col- lecting additional data from interviewed doctors, nurses, and hospital personnel in charge of each of these activities, the results of these efforts were used to determine the best theo- retical distribution to represent each stage of the process under study. It was determined that the interarrival times of walk-in patients follow an exponential distribution with a mean value that depends on the time of the day, as shown in Table 10.3. The interarrival times of ambulance patients follow an exponential distribution with a mean value of 30 minutes. The routing probabilities of patients at each stage inside the system are shown in Figure 10.14. The service time distributions and the values of their parameters are shown in Table 10.4. Due to the hospital request for information privacy, especially in budget data details, budget data were recoded in terms of budget units (BU). The cost units for the staff are as follows: 0.4 BU per receptionist, 1.2 BU per doctor, 0.5 BU per lab technician, and 0.3 BU per treatment or emergency nurse.
1. Build an ExtendSim model that simulates the operation of the emergency room department and that collects cycle time information for Category 1 patients. Set up the model to simulate 100 days (in the Simulation Setup dialogue under the Run Menu). Use trial and error to find the minimum staffing levels that will TABLE 10.3
Mean Interarrival Times (in minutes) for Walk-in Patients
 0:00 2:00 11.43 15.79
4:00 6:00 8:00 10:00 12:00 14:00 16:00 20.00 12.50 8.57 7.27 6.67 7.74 8.57
TABLE 10.4
Activity Times for Emergency Department
18:00 20:00 7.50 9.23
22:00 18.43
   Activity
Reception
Lab tests Examination Reexamination Minor treatment Major treatment
Distribution of Processing Times
  Uniform between 5 and 10 minutes
Triangular with parameter values of 10, 20, and 30 minutes Uniform between 10 and 20 minutes
Uniform between 7 and 12 minutes
Uniform between 20 and 30 minutes
Uniform between 60 and 120 minutes
  keep the average cycle time for Category 1 patients under 3.5 hours. Hint: Click on the “ExtendSim Help ...” item in the Help menu to access the User Guide. Search for “Random intervals with dynamic parameters.” This section of the User Guide explains how to combine the Create block and the Lookup Table block to generate items for which the mean interarrival time changes during the simulation.
2. Add the Optimizer block to the simulation model. Use the Clone Layer tool to add the initial value of each of the Resource Pool blocks to the Optimizer block. This creates five decision variables in the Optimizer block. Also add the average cycle time for Category 1 patients to the Optimizer block. Set up an optimization model that minimizes the average cycle time for Category 1 patients while restricting the labor budget to 10 BU. Set up the simulation for 30 days and the Optimizer to run one sample per case (Run Parameters tab).
3. Compare the two solutions found in Parts 1 and 2 using simulation runs of 100 days. The comparison should be made in terms of cost, average and maximum cycle time for Category 1 patients, and utilization of all resources.
