# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**:KANNAN N
* **Register Number**: 212223230097
* **Date of Submission**: 18.05.2026

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

First, I logged in to the AWS Management Console.

I navigated to the EC2 Dashboard.

I explored the Elastic Block Store (EBS) section under EC2.

I observed different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

I clicked on “Volumes” and selected “Create Volume.”

I chose the required volume type (General Purpose SSD – gp3).

I entered the desired storage size (for example, 8 GB).

I selected the same Availability Zone as my running EC2 instance.

I clicked on “Create Volume” to create the EBS volume.

After the volume was created, I selected the volume and clicked on “Attach Volume.”

I selected my running EC2 instance and attached the volume as a new device (for example, /dev/xvdf).

I connected to my EC2 instance using SSH from the terminal.

I checked the attached disk using the command lsblk to verify the new volume.

I formatted the attached volume using the command: sudo mkfs -t ext4 /dev/xvdf

I created a directory to mount the volume using: sudo mkdir /mnt/ebs

I mounted the volume to the directory using: sudo mount /dev/xvdf /mnt/ebs

I verified that the volume was mounted successfully using the df -h command.

I created sample files inside the mounted directory using: sudo touch /mnt/ebs/sample.txt

I stored some sample data inside the file.

I rebooted the EC2 instance from the AWS Console.

After rebooting, I reconnected to the instance using SSH.

I checked the mounted directory and verified that the stored data was still available.

This confirmed that the EBS volume provides persistent storage even after instance reboot.
---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="593" height="607" alt="image" src="https://github.com/user-attachments/assets/2c69b365-dbf7-483b-8ce1-1ffc106c581e" />

---

### Screenshot 2: EBS Volume Attached to EC2
<img width="1919" height="967" alt="1" src="https://github.com/user-attachments/assets/d53adbcf-2dfd-4170-a5b3-401bc0e3f488" />
<img width="1919" height="748" alt="2" src="https://github.com/user-attachments/assets/98f647b3-a2d3-4b90-83b5-aee7d21c19ce" />
<img width="1919" height="749" alt="3" src="https://github.com/user-attachments/assets/9909e348-f7ba-4057-8ab5-5eb10605f9cc" />

---

### Screenshot 3: Mounted Volume with Data
<img width="1918" height="965" alt="4" src="https://github.com/user-attachments/assets/507f6d08-c317-451f-8d2e-ad7f616fb5e8" />
<img width="1908" height="970" alt="5" src="https://github.com/user-attachments/assets/26e71380-ce6a-4807-be24-4fc70d4869a4" />

---

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
