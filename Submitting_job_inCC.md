# Basic - submitting job in Slurm Graham and Cedar
to access the cluster
```bash
ssh username@graham.computecanada.ca
ssh username@cedar.computecanada.ca
```
Submitting and check on job status
```bash
#submit a job
sbatch 

#check on the status of job submitted
squeue -u songxy

# list resources used by completed job
 sacct -j jobID [--format=JobID,MaxRSS,Elapsed] 
```
Loading and checking modules/softwares
```bash
module avail <name> # search for a module
module spider <name> # will give info about the module name and its dependcies
module list # show currently loaded modules
module load moduleName
module unload moduleName
module show moduleName # show commands in the module
```

Link to useful intro or resource:
- available programs: https://docs.computecanada.ca/wiki/Available_software
- check the cluster status: https://status.computecanada.ca/
- introduction ppt: https://www.westgrid.ca/files/WestGrid-July2017TownHall-CedarDemo.pdf
