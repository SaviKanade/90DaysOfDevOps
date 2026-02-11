Challenge Tasks



* Commands with screenshots :
Task 1:
lsblk
lvm
pvs
Snap :
<img width="646" height="373" alt="Screenshot 2026-02-11 at 1 14 13 PM" src="https://github.com/user-attachments/assets/7fbcd571-23ac-4061-bbdd-4a8a920e6a21" />


Task 2: 
pvcreate /dev/nvme1n1   
pvcreate /dev/nvme2n1
pvs

Snap :
<img width="501" height="171" alt="Screenshot 2026-02-11 at 1 14 56 PM" src="https://github.com/user-attachments/assets/a1f2c436-c810-4eec-8d3a-cf01e1535cdf" />
<img width="623" height="406" alt="Screenshot 2026-02-11 at 1 20 03 PM" src="https://github.com/user-attachments/assets/82ceac35-00c9-44ac-a367-63568b4eae41" />


Task 3:
vgcreate devops-vg /dev/nvme1n1 /dev/nvme2n1
vgs

Snap :
<img width="661" height="133" alt="Screenshot 2026-02-11 at 1 21 40 PM" src="https://github.com/user-attachments/assets/6321945c-3710-4d8f-a7ff-7922ebb2d6b3" />


Task 4:
lvcreate -L 500M -n app-data devops-vg
lvs

Snap :
<img width="817" height="136" alt="Screenshot 2026-02-11 at 1 24 15 PM" src="https://github.com/user-attachments/assets/75beee2a-a84f-48ef-a501-84d2304bdf4b" />


Task 5:
mkfs.ext4 /dev/devops-vg/app-data
mkdir -p /mnt/app-data
mount /dev/devops-vg/app-data /mnt/app-data
df -h /mnt/app-data

Snap :
<img width="694" height="323" alt="Screenshot 2026-02-11 at 1 26 57 PM" src="https://github.com/user-attachments/assets/96bacb4c-b895-4174-bb82-e8051d3619b7" />


Task 6:
lvextend -L +200M /dev/devops-vg/app-data
lsblk
resize2fs /dev/devops-vg/app-data
df -h /mnt/app-data

Snap :
<img width="1012" height="627" alt="Screenshot 2026-02-11 at 1 31 00 PM" src="https://github.com/user-attachments/assets/df52311a-3061-4acb-9b75-eb2b0b193209" />



* What you learned (3 points)
1. I was aware of mounting point but learned from basic as how we get the sizes.
2. Learned about volume storages(physical/logical/volume group).
3. Learned about disk/volume formatting as well. Initially didnot understand it but later on got to know to freeup the space to use for mounting that's why we are using mkfs.ext4 command.
   
