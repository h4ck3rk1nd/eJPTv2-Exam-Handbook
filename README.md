![1_jwmm8318giyrlhr_Im_laQ](https://github.com/user-attachments/assets/e0932c9c-addd-42d3-812a-40cbc6977a96)

# eJPTv2-Exam-Handbook
## A collection of important notes that is helpful during the eJPTv2 examination.

### Assessment Methodologies
      $ host <www.example.com> -- DNS lookup Utility
      $ fping -a -g 192.168.1.0/24 2>/dev/null -- For PING Sweep
      $ nmap -sn 192.168.1.0/24 
      
      ------------ or a bash script --------------------
      
      #!/bin/bash
      # Check if subnet is provided
      if [ "$#" -ne 1 ]; then
          echo "Usage: $0 <subnet>"
          echo "Example: $0 192.168.1"
          exit 1
      fi
      SUBNET=$1
      # Perform ping sweep
      for i in {1..254}; do
          ping -c 1 -W 1 "$SUBNET.$i" &> /dev/null && echo "Host $SUBNET.$i is up" &
      done
      wait
      
      
### Host & Networking Auditing
### Host & Network Penetration Testing
### Web Application Penetration Testing
