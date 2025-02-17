# ⏰Splunk SIEM Monitoring Solution Project


## 📺Scenario
Played the role of a SOC analyst at a company called VSI. VSI has received information that another company, JobeCorp, may launch cyberattacks to disrupt VSI’s business. We were tasked with using Splunk to develop a monitoring solution to monitor Windows Server, which runs many of VSI's back-end operations. This monitoring solution can protect against potential cyberattacks on VSI’s systems. 


## 🎯Task
Developed and designed a custom monitoring environment as part of the cyber security incident response in order to protect a fictional organization from potential cyberattacks using Splunk SIEM (Security Information and Event Management).


## 🔑Key Achievements
1. Loaded and analyzed logs (Windows Server Logs) to gain insights into server activities and establish a baseline for normal behavior. This baseline helps detect anomalies by analyzing key parameters such as severity levels, failed and successful events, event volume, signatures, and user activity.

2. Designed and implemented a custom monitoring solution such as alerts, reports and dashboards based on the established baseline. These alerts automatically notify the designated security personnel via email whenever activity surpasses the defined threshold, enabling real-time detection and response to potential threats.

3. Loaded new logs (Window Server Attack Logs) that cover the time period during which the attack occurred. Analyzed these new attack logs with our monitoring solution to determine the efficacy of our solution. 

4. Strengthened monitoring capabilities by integrating a user-friendly dashboard within the Splunk app. This enhanced visibility into security events, providing a more comprehensive view of data to improve threat detection and defense against cyberattacks.

## 🖥️Technologies Used
Splunk SIEM

## ⌨️Languages Used 
SPL (Splunk Search Processing Language)

## 📜Logs Analyzed 

- Two sets of logs were analyzed:
   1. Windows Server Logs
   2. Windows Server Attack Logs


## 📸Screenshots 

**Windows Server Log** 

**Report Analysis for Severity**

Did you detect any suspicious changes in severity?

   - After the attack, the informational category had a 13% decrease (went from  93% to 80%) and the high category had a 13% increase (went from 7% to 20%). Yes, there were suspicious changes in severity level since the high category increased. 

Normal log:
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20log%201.png?raw=true)


Attack log:
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20attack%20log%201.png?raw=true)



**Report Analysis for Failed Activities**

Did you detect any suspicious changes in failed activities?

   - Yes, we did see a slight change in failed activities. The number of successful activities increased by 1% and the number of failed activities decreased by 1%. 

Normal log: 
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20log%202.png?raw=true)

Attack log:
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20attack%20log%202.png?raw=true)


**Alert Analysis for Failed Windows Activity**

Did you detect a suspicious volume of failed activity?

   - Yes, there was a suspicious volume of failed activity after the attack at 8 AM on Wednesday, March 25th, 2020. 

Normal logs: 
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20log%203.png?raw=true)


Attack logs: 
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20attack%20log%203.png?raw=true)


If so, what was the count of events in the hour(s) it occurred?

   - The count of failed Windows activity was 35. 


When did it occur?

   - At 8AM on Wednesday, March 25th, 2020.


Would your alert be triggered for this activity?

   - Yes, the threshold was set to >15 so the alert would have been triggered since it is within the trigger threshold. 


After reviewing, would you change your threshold from what you previously selected?

   - No, I wouldn’t change the threshold because reviewing the normal logs activity we concluded that it was low enough to trigger the alert yet high enough to prevent any false positives. 

   
**Alert Analysis for Successful Logins**

Did you detect a suspicious volume of successful logins?

   - Yes, there is a suspicious volume of successful logins on the attack logs compared to the normal logs but the amount of logins reduced drastically after the attack. 

Normal logs:
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20log%204.png?raw=true)


Attack logs: 
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20attack%20log%204.png?raw=true)


If so, what was the count of events in the hour(s) it occurred?

   - From the attack logs, we noticed that at 8AM there were 16 successful logins then at 9AM there were only 4 successful logins then from 10AM to 11AM there were 0 logins. 


Who is the primary user logging in?

   - The primary user logging in was user_a, they had a huge number of logins compared to other users at 2:30 AM with the login count of 10.

Normal logs:
![alt _log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20log%205.png?raw=true)


Attack logs: 
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20attack%20log%205.png?raw=true)



When did it occur?

   - On Wednesday, March 25th, 2020 at 2:30 AM.


Would your alert be triggered for this activity?

   - No, our alert wouldn’t have been triggered because we set our threshold to >26 successful logins an hour to alert the SOC and from the attack logs, we see that the successful logins decreased with max. number of successful logins being 16 which is less than 26, which is not within our threshold. 


After reviewing, would you change your threshold from what you previously selected?

   - After reviewing, I think we would need more log files and historical data to be examined in order to determine the threshold. Since there was a lack of logins after the attack in this scenario which indicates suspicious activity, we could have an alert if the amount of logins decreases significantly to a certain number per hour. 


**Alert Analysis for Deleted Accounts**

Did you detect a suspicious volume of deleted accounts?  
   
   - Yes, there was a suspicious volume of deleted accounts in large amounts from 9AM to 11AM.

Normal log: 
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20log%206.png?raw=true)


Attack log:
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20attack%20log%206.png?raw=true)


**Dashboard Analysis for Time Chart of Signatures**

Does anything stand out as suspicious?

   - Yes, there are two main signatures that stand out on the attack logs compared to the normal activity logs.

Normal log: 
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20log%207.png?raw=true)

Attack log:
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20attack%20log%207.png?raw=true)



What signatures stand out?

   - A user account was locked out 
An attempt was made to reset an account password 

  What time did it begin and stop for each signature?

   - A user account was locked out began at 1AM and stopped at 2AM. An attempt was made to reset an account password began at 9AM and stopped at 10AM.

What is the peak count of the different signatures?

   - A user account was locked out: peak count = 896
An attempt was made to reset an account password: peak count = 1,268


**Dashboard Analysis for Users**  

Does anything stand out as suspicious?

   - Yes, there are two users with increased activity on the attack log that stand out.
     
Normal logs:
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20log%208.png?raw=true)


Attack Logs:
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20attack%20log%208.png?raw=true)


Which users stand out?

   - User_a and user_k


What time did it begin and stop for each user?

   - Increased user activity of user_a began at 1AM and stopped at 2AM. 
Increased user activity of user_k began at 9AM and stopped at 10AM. 


What is the peak count of the different users?

   - User_a: peak count = 984
User_k: peak count = 1,256


**Dashboard Analysis for Signatures with Bar, Graph, and Pie Charts**

Does anything stand out as suspicious?

   - Yes, comparing the normal activity logs to the attack logs, we can see that there are two signatures with increased activity that stand out as suspicious.

Normal Logs:
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20log%209.png?raw=true)


Attack Logs: 
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20attack%20log%209.png?raw=true)


Do the results match your findings in your time chart for signatures?    

   - Yes, they match our findings in the time chart for signatures. 
The two signatures that increased significantly were: A user account was locked out and An attempt was made to reset an accounts password for both the time chart and total count for signatures findings. 


**Dashboard Analysis for Users with Bar, Graph, and Pie Charts**

Does anything stand out as suspicious?

   - Yes, user_a and user_k stand out as suspicious because their activity has increased significantly. 


Normal log: 
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20log%2010.png?raw=true)


Attack logs:
![alt log](https://github.com/ayushmak7/Splunk-SIEM-Defensive-Project/blob/main/images/windows%20attack%20log%2010.png?raw=true)


Do the results match your findings in your time chart for users?

   - Yes, the results match our findings in our time chart for users. User_a and user_k had increased activity for both. 


**Dashboard Analysis for Users with Statistical Charts**

What are the advantages and disadvantages of using this report, compared to the other user panels that you created?

   - The statistical time charts for signatures and users provide us with more detailed answers if you know what you’re looking for, especially on the signature count or user activity per hour chart. A disadvantage of using statistical report would be that it doesn’t give us visualizations like using a line/bar/pie chart would, for example, if there is a suspicious activity, we want to look for it quickly and examine the trends such as spikes and dips occurring in an event so we can better prepare for such attacks in the future. 




