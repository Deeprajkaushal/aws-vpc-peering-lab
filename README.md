# AWS VPC Peering Lab

## Project Overview
This project demonstrates AWS VPC Peering by establishing private network connectivity between two Virtual Private Clouds (VPCs) in the AWS Europe (Stockholm) region (`eu-north-1`).

## Architecture

- **VPC A:** `10.10.0.0/16`
- **VPC B:** `10.20.0.0/16`
- **VPC Peering Connection:** `pcx-0c857e64f45cde627`
- **VPC A EC2 private IP:** `10.10.1.203`
- **VPC B EC2 private IP:** `10.20.1.29`

## AWS Services Used
- Amazon VPC
- VPC Peering
- Amazon EC2
- Route Tables
- Security Groups

## Implementation
1. Created two VPCs with non-overlapping CIDR ranges.
2. Created subnets and launched EC2 instances in both VPCs.
3. Established a VPC Peering connection.
4. Added routes to both VPC route tables.
5. Configured security groups to allow ICMP traffic for connectivity testing.
6. Verified private communication using the `ping` command.

## Connectivity Test

Command executed from the EC2 instance in VPC A:

```bash
ping -c 4 10.20.1.29
```

**Result:** 4 packets transmitted, 4 received, 0% packet loss.

This confirms successful private connectivity between the two VPCs.

## Key Learnings
- VPC CIDR planning
- VPC Peering configuration
- Route table configuration
- Security group rules
- EC2 connectivity testing

## Conclusion
Successfully configured and tested AWS VPC Peering between two VPCs using private IP addresses.
