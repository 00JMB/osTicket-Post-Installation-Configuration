<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket - Post-Install Configuration

This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.

---

## 💻 Environments and Technologies Used

- **Microsoft Azure:** Virtual Machines/Compute
- **Remote Desktop**
- **Internet Information Services (IIS)**

---

## 🖥️ Operating Systems Used

- **Windows 10 (21H2)**

---

## 🎯 Post-Install Configuration Objectives

- Configure Roles

* Configure Departments
* Configure Teams
* Configure Agents
* Configure Users
* Configure SLA
* Configure Help Topics

---

## 📂 Preface

Before we begin, here are the two links we’ll need for this process:

- **Admin/Agent Login Page:**
  [http://localhost/osTicket/scp/login.php](http://localhost/osTicket/scp/login.php)

- **End Users osTicket URL:**
  [http://localhost/osTicket](http://localhost/osTicket)

I’ll make sure to specify which Panel we’re using during each specific section.

---

## 🚀 Configuration Steps:


### 🧮 Roles (A group of permissions attributed to an Agent/Analyst)

* Go to the **Admin/Agent** link > Click **Admin Panel** (top right corner)

* Click **Agents tab** > **Roles** > **Add New Role**
![image](https://github.com/user-attachments/assets/f41de2b4-4cc4-41c2-bc04-19da8663e030)

* Name the new role: **Supreme Admin** > Define Permissions > Enable all under **Tickets**, **Tasks**, & **Knowledgebase**![image](https://github.com/user-attachments/assets/d45821cc-f715-4674-a993-c7b93de30677)![image](https://github.com/user-attachments/assets/393d88fa-08e7-45dc-92bd-be818283b273)![image](https://github.com/user-attachments/assets/df544e52-50d3-4d76-9ce7-5843fee3cd7c)

* Click **Add Role** to confirm


---

### 🏢 Departments ( used to define Ticket Visibility; e.g., Help Desk vs SysAdmins vs Networking)

* **Admin Panel:**
  
* **Agents tab** > **Departments** > **Add New Department**
* Set **Parent** to **Top-Level Department** > Name it **SysAdmins**![image](https://github.com/user-attachments/assets/4c793e52-4943-4934-a3fd-5149cd1d253a)
* Scroll down and click **Create Dept**


---

### 👥 Teams (A way to group Agents from different Departments)

* **Admin Panel:**

* **Agents tab** > **Teams** > **Add New Team**
* Name the team: **Online Banking** > **Create Team**


---

### 👩‍💼 Agents (Our Help Desk Analysts)

* **Admin Panel:**

* **Agents tab** > **Add New Agent**

* Name the first agent **Jane Doe** > Set a fake email and username![image](https://github.com/user-attachments/assets/5ca68c93-1a78-4136-bbe9-8f90892e1fdd)

* **Set Password** > Set a password > uncheck **Require password change at next login** > ** click Set**![image](https://github.com/user-attachments/assets/24b9533a-8c11-4fca-b58c-7d5a2b59e443)

* **Access Tab** > Primary Department: **SysAdmins**, Role: **Supreme Admin**![image](https://github.com/user-attachments/assets/cae2c81f-fabe-466f-baf5-321ecb0e3175)

* **Teams Tab** > Add **Jane Doe** to **Online Banking team**![image](https://github.com/user-attachments/assets/a3f5fc77-33e0-4684-a61a-4e1f2ddf7a4e)

* Repeat creation process for another agent, **John Doe**

* Assign them a standard **Support** role with **Expanded Access** permissions
  
* **Keep track of the log in information you’ve assigned both accounts! (As well as the Users in the next section)**


---

### 👤 Users (Our Customers/Cx that need support)

* **Agent Panel:**

* **Users tab** > **User Directory** > **Add User**![image](https://github.com/user-attachments/assets/2b7da8e5-67f3-478c-9f77-0978575e7463)

* Set a name and email for your demo user![image](https://github.com/user-attachments/assets/daef6099-dd3e-40bc-a358-0fd68e8ff272)


---

### ⏱️ SLA: Service Level Agreement (A measurement of ticket severity + How long before a ticket is marked as “overdue”)

* **Admin Panel**

* **Manage tab** > **SLA** > **Add New SLA Plan**![image](https://github.com/user-attachments/assets/59aac491-5368-4118-b601-563f533eff1e)

* Create **Sev-A** > Grace Period: **1 (hour)** > Schedule: **24/7**![image](https://github.com/user-attachments/assets/c2f2b8c8-5b47-4e8a-ad95-14555ad43fe6)

* Create **Sev-B** > Grace Period: **4 (hours)** > Schedule: **24/7**

* Create **Sev-C** > Grace Period: **8 (hours)** > Schedule: **Monday - Friday: 8am - 5pm…**


---

### 📑 Help Topics (Categories End-Users have for ticket creation)

* **Admin Panel:**
  
**Manage tab** > **Help Topics** > **Add New Help Topic**![image](https://github.com/user-attachments/assets/bef58543-64d4-4d1f-8bfc-87dbe56200ba)

* Topic: **Business Critical Outage** > Parent Topic: **Report a Problem** > **Add Topic**![image](https://github.com/user-attachments/assets/f5699f2e-80d0-49af-8bf9-00241df73f65)

* Topic: **Personal Computer Issues** > Parent Topic: **Report a Problem** > **Add Topic**
* Topic: **Equipment Request** > Parent Topic: **General Inquiry** > **Add Topic**
* Topic: **Password Reset** > Parent Topic: **Report a Problem** > **Add Topic**
* Topic: **Other** > Parent Topic: **General Inquiry** > **Add Topic**


---

### 🎯 Next Steps

You're now ready to move on to the final part of our osTicket project: **[osTicket: Ticket Lifecycle Examples](https://github.com/00JMB/osTicket-Ticket-Lifecycle-Examples)**
