# dq-tf-cloudwatch-ec2

Cloudwatch module for EC2 monitoring using the following components:

- SNS
- Cloudwatch
- IAM
- Lambda
- Python

# Usage

```
module "cloudwatch_alarms_ec2" {
  source         = "github.com/UKHomeOffice/dq-tf-cloudwatch-ec2"
  environment    = "notprod"
  naming_suffix  = "${local.naming_suffix}"
  ec2_instance_id = "${aws_instance.instance.id}"
  pipeline_name  = "foobar"
}
```

# Supported variables

| Variable name | Required | Description |
| :---: | :---: | :---: |
| environment | __True__ | Environment name |
| naming_suffix | __True__ | Tag naming variable |
| ec2_instance_id | __True__ | EC2 instance ID |
| pipeline_name | __True__ | Tag name |
