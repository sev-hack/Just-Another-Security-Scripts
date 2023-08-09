# Just Another Security Scripts
 
Just small scripts

## Scan docker images using Trivy

Use this command if you want to scan **running** docker images on the machine and generate reports:
```bash
for i in $(sudo docker ps --format "{{.Image}}"); do trivy image $i -o trivy-report-for-$(echo $i | sed 's#/#_#g').txt ; done
```

