## Getting Started


1. Create a Google Cloud VM with 4vCPU 2 cores and 16gb of memory
2. Staging
   * Upload the ``docker-compose.yml`` and ``nbs`` directory to the virtual machine
   * clone the project ``git clone https://github.com/Cormac-Flanagan/Report-INFS3208.git``
3. download the dataset into the directory from https://www.dropbox.com/scl/fo/8dk01mj02s0pp2whym1ai/AD130IGGeFOlFk0COuZHlJQ?rlkey=vwqf6a9jwv8ouhxkp1s8u6dsr&st=yzwqmow0&dl=0
   * Project directory should look like nbs/[report.ipynb, archive/*, *.csv]
3. In the terminal Run ``docker-compose -f docker-compose.yml up``
4. Expose port 8888 and 8080 of the VM to external traffic or setup an SSH Tunnel
   *  ``gcloud compute ssh YOUR_VM_NAME --zone YOUR_ZONE -- -L 8888:localhost:8888``
   *  Create a Firewall rule that allows tcp:8888 connections and then attach it the VM and connect VM's external IP
