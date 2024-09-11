# VSD-SoC-Design-Program

L1: OpenLANE Working Directory Structure

Linux Commands

cd: Change directory

ls: list files 

ls -ltr: List the files in chronological order

ls --help: Gives the detailed information about commands


![linuxcommands](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/63a389c8-6025-4b6a-b103-423c875d2234)

clear command

![clear command](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/f2ae3a86-117f-4f20-9e36-fae8524a5957)

pdks

![image](https://github.com/user-attachments/assets/ae30cb39-ac12-4577-9616-f0ed076f6f09)

libs.ref, libs.tech

![libs](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/e0d718bf-fb9a-4c3c-adf4-b39538f1029e)

sky130_fd_sc_hd

![sc](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/371b3f31-fc41-466e-a0f1-13aa1b433bfb)

To invoke the tool
docker 
./flow.tcl -interactive

![openlane](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/ff642715-c5eb-4d00-ba6d-6e265974a857)

L2: Design Preparation Steps

package require openlane 0.9

prep -design picorv32a

![image](https://github.com/user-attachments/assets/81ac7fd4-eab3-466a-b63c-c21972e30519)


Various designs in openlane

![image](https://github.com/user-attachments/assets/5247ca15-3106-41f6-9d2e-ac08518d29a3)


picorv32a contains 3 files

src: source file

pdk specific file 

config.tcl file


![picorv32a](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/d2a79fd2-80bd-48c0-a2ce-f5774ba23fa5)

less config.tcl contains all the information

design environment

verilog file

sdc file

clock period

setting of the file

![config](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/b96eec9a-2f3b-4fb3-b0f3-841cc905029a)

Design Preparation steps

![designprep](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/0afd49ae-0dce-45e3-bd30-abf0a46f76c3)

runs directory is created

![image](https://github.com/user-attachments/assets/4f42fd2f-da7f-4ceb-9204-0797654ef11e)

folder structure required for openlane

![image](https://github.com/user-attachments/assets/ec9d0422-17ba-4f23-9f23-ee25b37a75d9)


cd tmp

![image](https://github.com/user-attachments/assets/aa92a1a7-376c-4bb7-902b-6705fef9ed3c)


less merged.lef

![merged](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/9695e7dc-e993-42b7-9800-28e9de3539ef)

cd runs

cd results

cd synthesis

![image](https://github.com/user-attachments/assets/1d0d297c-0f0a-4cbd-93a8-0c32ff13a2d3)


cd reports

![image](https://github.com/user-attachments/assets/a08e67c5-d40f-4d3e-8525-ad173780451d)

less config.tcl: it shows the default parameters taken by run

![configtcl](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/2f878d07-9a84-4b6f-99f7-cf421c88303d)

run_synthesis

![synthesis](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/45f0224d-1e11-428e-a314-e597a21e876e)

cd results/synthesis: shows the verilog file of design

![image](https://github.com/user-attachments/assets/301ecbdb-dc2e-455c-bcfa-ff04fc01e920)


cd reports/synthesis

![image](https://github.com/user-attachments/assets/fecc4c51-56cd-47db-9868-2bea9ae4e28c)

Actual synthesis statics report from this we calculate the flop ratio

command to get the synthesis reports

![image](https://github.com/user-attachments/assets/3e5d2653-f380-4c3c-8145-b6f345dddb2d)


![image](https://github.com/user-attachments/assets/11931170-4ca0-446a-81e7-1ad6169b035c)

Flop ratio

![flopratio](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/8bb0301f-90e1-4417-93ae-c62e774f75ee)

sta timing report

![image](https://github.com/user-attachments/assets/e1d15e6c-8c47-4905-908c-f912011c604b)

floorplan: set the die area, core area, aspect ratio, utilization factor, place the input output cells, power distribution network and macrocell placement

standard cells are not placed in floor planning


Just go to to the location given in the screenshot and try to open the readme file

![image](https://github.com/user-attachments/assets/09b4e8dc-9cc0-4e8b-b5ef-125929b1b426)

README.md file by giving the command less README.md: Here you can see the variables required for each stage, these variables are noting but switches

![image](https://github.com/user-attachments/assets/db8fc66e-ae66-4ad2-9c1b-1bb486683e45)

To see the default settings of the floorplan type the following command

less floorplan.tcl

In the screenshot FP_IO_MODE 1 indicates that the pins are positioned randomly around the core but at equi distant for zero they will not be at equi distant

![image](https://github.com/user-attachments/assets/12933317-3809-4277-afd3-566afcb27335)

less config.tcl: shows design name, clock period etc


![image](https://github.com/user-attachments/assets/3ce7b835-5017-4305-8006-f5009edb62ef)



To run the floor plan just give the command as run_floorplan

![aspectratioo](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/a8abead7-877d-4aca-825a-860c3f8dc6f3)

![floorplan](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/cf5c3f91-6a1b-4bcb-91d6-9f948a698f81)

![1dieaarea](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/429b50f4-6d1a-4833-8c19-b78b1481d945)


default parameters set for floorplan in openlane

![image](https://github.com/user-attachments/assets/cb6d9c56-2ff3-4701-b490-4b4d4be5d869)


logs/floorplan/

![image](https://github.com/user-attachments/assets/42725de1-0913-4281-98a9-5921d53eb1dd)

ioPlacer.log

![image](https://github.com/user-attachments/assets/aa1b3bc6-12d0-4b36-800f-c3435812c074)

![image](https://github.com/user-attachments/assets/3122ac0c-7435-4ae3-908a-4485af0d73d8)

def file: design exchange format

![image](https://github.com/user-attachments/assets/d454d048-4c93-4cfe-b56d-f37ff41edda5)

beginning of def file is diearea

![image](https://github.com/user-attachments/assets/a55c59ac-9ce0-4970-9826-3381e0069a15)

![image](https://github.com/user-attachments/assets/31d96e7c-b548-4ad2-9a5b-b02977cc4692)

Press s and v to fit it on screen properly

![image](https://github.com/user-attachments/assets/f5c6b1c7-e9e5-4c81-bd97-f91646c2d2f4)

![image](https://github.com/user-attachments/assets/1e31bcb4-ebb7-437f-9a99-366d76de6328)

move the cursor on particular object and then press s

go to tkcon main and type what it will show the details as in the screenshot

![image](https://github.com/user-attachments/assets/06538254-9343-49e2-bb8e-95cd7b83ea84)

cd Desktop/work/tools/openlane_working_dir/openlane

git clone https://github.com/nickson-jose/vsdstdcelldesign

![10](https://github.com/VijayalaxmiSKumbhar/VSD-SoC-Design-Program/assets/170864002/46645870-db68-4a72-8829-a900744dcd50)

Various files in vsdstdcelldesign

![image](https://github.com/user-attachments/assets/ec21011e-cd72-43af-857b-dc43fcf9f064)

tech file

![image](https://github.com/user-attachments/assets/1cfe424e-d118-44e5-9fdb-a6fff86b2de2)

copying the sky130A.tech file

![image](https://github.com/user-attachments/assets/135f44aa-d471-404c-8b14-70a3e4dadf94)

Aftercopying the file will be seen as given in the screenshot

![image](https://github.com/user-attachments/assets/1145bf1c-8364-4f53-9e7c-bd71c0987487)

inverter in magic

![image](https://github.com/user-attachments/assets/3fa8b21b-038d-4ec2-85bb-d548212d552f)

press s & V to fit on screen properly

![image](https://github.com/user-attachments/assets/10f9f197-ca75-4fe5-a9f8-bd6b81944874)

what in tkcon tells highlighted portion, so here NMOS is identified

![image](https://github.com/user-attachments/assets/b7b14fb4-70f1-4425-9a84-d30a008dd39b)

PMOS is identified

![image](https://github.com/user-attachments/assets/20943225-513a-4192-8028-17edf13ffe91)

In magic to see whether two different parts of the circuit are connected press s two times

first time press: the area where the cursor is highlighted

![image](https://github.com/user-attachments/assets/c88e01f1-7878-40bd-a841-9332c12ed11b)


second time press:the area where it is connected gets highlighted

![image](https://github.com/user-attachments/assets/c03bb8c0-566a-4e1f-bc60-fb4d1ee97fbc)

extract on spice

![image](https://github.com/user-attachments/assets/3b3808b4-d487-4d7a-8a4f-bbc74295f80d)

spice file has been created

![image](https://github.com/user-attachments/assets/dbe87655-b6df-4ca8-a65e-d33016a3090e)

let us see what is inside this spice file by giving the command vim sky130_inv.spice

![image](https://github.com/user-attachments/assets/db164868-3b01-41f4-88ed-980b77650c3b)

edited spice file

![image](https://github.com/user-attachments/assets/71d34498-ef4b-4dd8-8254-223e999ddc1d)

to simulate the spice file give the command ngspice sky130_inv.spice

![image](https://github.com/user-attachments/assets/9bb9f34a-1b7e-4509-a9c6-3af0160ff43f)

to see the plot give the command as plot y vs time a

![image](https://github.com/user-attachments/assets/f8e17bb9-d30d-4d99-aefe-8ea98f87f2f7)

to remove the spikes in the output waveform we will change the load capactice value to 2fF

![image](https://github.com/user-attachments/assets/8e896688-1e6b-48ec-907b-6c0d127f5a61)

20% Screenshots
![image](https://github.com/user-attachments/assets/66b776dd-f78d-487b-a15d-8895199c6607)

![image](https://github.com/user-attachments/assets/874689f3-07fa-4d4a-a991-97168bab0198)

80% screenshots

![image](https://github.com/user-attachments/assets/3cf3d08e-989e-45b1-b72a-7cb9a47e16eb)

![image](https://github.com/user-attachments/assets/b6f9e2f3-65e6-464d-a394-d66d55c989d1)

Rise time= 2.24608e-09 - 2.18196e-09=0.06412 nS

Now let us calculate the propogation delay

50% screenshots

![image](https://github.com/user-attachments/assets/82afc187-6152-436e-856f-cd1c43850e18)

![image](https://github.com/user-attachments/assets/eb6f65af-2cfc-47e4-a476-6ee78ba92e53)

cell rise delay = 2.21183e-09 - 2.15108e-09 = 0.06075 nS


#extracting lef file out of .mag file

less tracks.info: tracks are basicaaly used during routing stage

![image](https://github.com/user-attachments/assets/13a0078d-6b01-4e26-869f-3729d7f22291)

Each of the tracks are placed at 0.46 along horizontal direction. Similarly for y direction 0.34

for every layer there is x and y direction

![image](https://github.com/user-attachments/assets/3cb49fbe-5f97-4cb0-8ef2-b0d2d37f77c6)

grid dimensions

![image](https://github.com/user-attachments/assets/356dd412-37cc-4c73-aaf8-4816bbfa5d25)

width of the standard cell must be odd multiples of xpitch

creating a port

select a particular region and then go to edit click on text to make the changes

![image](https://github.com/user-attachments/assets/ede1d061-b743-4fcd-9cfe-96a201fea458)

port class and port use

what will tell you to which layer it is attached, port name, signal etc

![image](https://github.com/user-attachments/assets/0bc83188-34e4-45d2-87ec-b9c7deb93532)

once this is done we are ready to extract the lef file

save the file as sky130_vsdinv.mag

![image](https://github.com/user-attachments/assets/82bffb63-b5a0-4307-b802-5f8fcfe475d9)

lef write

![image](https://github.com/user-attachments/assets/0023a960-8391-42eb-af79-6f4c4d6c134f)

type the following commands to open the lef file

![image](https://github.com/user-attachments/assets/87a68d3f-aa81-46b5-a163-efaaf38d01ec)

![image](https://github.com/user-attachments/assets/283da182-302c-4a5a-8eef-6d11ce9e7cdf)

plug this lef file into our picorv32a

![image](https://github.com/user-attachments/assets/b542a447-3dd5-4a7f-911d-020fd1442194)

copying lef file into src

![image](https://github.com/user-attachments/assets/7efa90b8-7327-406d-b3da-b31fcbd28ecc)

The lef file has been included

![image](https://github.com/user-attachments/assets/751a16b0-376d-4f93-bace-2b7b60dd1793)

less sky130_fd_sc_hd__typical.lib

![image](https://github.com/user-attachments/assets/115aa230-cb68-4132-bdc6-c81f7527868b)


![image](https://github.com/user-attachments/assets/0e052742-44fe-49ea-88e4-24245c1a185f)

src will be having lef file as well as library

![image](https://github.com/user-attachments/assets/29f3947c-a431-453f-ac29-7c04b5c11a6d)

![image](https://github.com/user-attachments/assets/b9b7a038-2700-429c-a33b-ec85b7b70e90)

now modify config.tcl

![image](https://github.com/user-attachments/assets/ff25f623-fdcd-4875-8b11-d0c1e7854481)



overwrite will take the new values defined in config.tcl

![image](https://github.com/user-attachments/assets/85ef28c4-798d-452b-8656-e5847cbb9235)

![image](https://github.com/user-attachments/assets/fc899c11-24f8-4c4b-ac3e-154425d5392d)

Additional steps

![image](https://github.com/user-attachments/assets/4f5cb375-cc59-4444-af07-3d83cf08b0ef)


mapping our custom vsd inverter 

![image](https://github.com/user-attachments/assets/177a2f1c-572d-428d-ba91-bcf72b67143d)

![image](https://github.com/user-attachments/assets/92118c9c-ef43-412e-b22b-85d3fb476b20)

Synthesis is successful. In the screenshot wns is maximum slack and tns is total negative slack

![image](https://github.com/user-attachments/assets/1671895d-e040-4686-af75-40cd09d51f84)




























