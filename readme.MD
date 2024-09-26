# Terraform AWS VPC Module customised

This module is going to create the follwing resources. For HA we are going to get first 2 AZ.

* VPC
* Inernet Gateway associated with vpc
* 2 Public subnets
* 2 Private subnets
* 2 Database subnets
* Database subnet group
* EIP
* NAT Gateway
* Public route table
* Private route table
* Databse route table
* Route table associations with subnets
* Peering with default VPC(if required)
* Peering routes in acceptor and requestor route tables


# Inputs
* Project_name(Mandatory): User must supply their project_name.
* environment(Mandatory): User must supply their environment_name.
* vpc_cid(Mandatory): User must supply their VPC_CIDR.
* enable_dns_hostname (optional): defaults to true.
* common_tags (optional): default is empty. User can supply tags in list(string) format.
* vpc_tags (optional): default is empty. User can supply tags in list(string) format.
* igw_tags (optional): default is empty. User can supply tags in list(string) format.
* public_subnet_cidr (Mandatory): User can supply 2 valid public subnet CIDR.
* public_subnet_tags (optional): default is empty. User can supply tags in list(string) format.
* private_subnet_cidr (Mandatory): User can supply 2 valid private subnet CIDR.
* private_subnet_tags (optional): default is empty. User can supply tags in list(string) format.
* databse_subnet_cidr (Mandatory): User can supply 2 valid database subnet CIDR.
* databse_subnet_tags (optional): default is empty. User can supply tags in list(string) format.
* db_subnet_group_tags (optional): default is empty. User can supply tags in list(string) format.
* nat_gateway_tags (optional): default is empty. User can supply tags in list(string) format.
* public_route_table_tags (optional): default is empty. User can supply tags in list(string) format.
* private_route_table_tags (optional): default is empty. User can supply tags in list(string) format.
* database_route_table_tags (optional): default is empty. User can supply tags in list(string) format.
* is_peering_required (optional): default to false
* vpc_peering_tags (optional): default is empty. User can supply tags in list(string) format.

# Outputs

* vpc_id: VPC ID created
* public_subnet-ids: list of 2 public subnet ids created
* private_subnet-ids: list of 2 private subnet ids created
* databse_subnet-ids: list of 2 database subnet ids created






