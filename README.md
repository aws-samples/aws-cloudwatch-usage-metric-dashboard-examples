## aws-cloudwatch-usage-metric-dashboard-examples

## Overview
Example CloudWatch dashboards for monitoring and managing API usage in AWS.
 - This repo is based on the steps outlined in this [article](https://aws.amazon.com/blogs/mt/managing-and-monitoring-api-throttling-in-your-workloads/).

## Getting Started

### Usage metrics

#### Sample dashboards

- AWS-Usage-Metrics-CloudWatch.txt
- AWS-Usage-Metrics-DynamoDB.txt
- AWS-Usage-Metrics-EC2.txt

#### To create an API usage dashboard widget example

- Open the CloudWatch console at https://console.aws.amazon.com/cloudwatch/.
- In the navigation pane, choose Metrics.
- From AWS Namespaces, choose Usage, and then choose By AWS Resource. This section will contain resources in your account that support usage metrics. The list will vary based on what is currently deployed.
- Choose the resource or API that you would like to monitor usage for.
- On the Graphed metrics tab, from Math expression, choose Common, and then choose SUM. Use the following values:
  - Id: m1
  - Label: Call Count
  - Period: 1 Minute
- From Math expression, choose Start with empty expression. Use the following values:
  - Id: e1
  - Label: Service Limit Quota
  - Details: SERVICE_QUOTA(m1) 
- From Actions, choose Add to dashboard.
- Select a dashboard or create one.
- For the widget time, use the default option (Line).
- Give the widget title a descriptive name (for example, <API_name> Usage vs. Quota).
- Choose Add to dashboard.

### EC2 API metrics

#### Sample dashboards

- AWS-EC2-API-Metrics.txt 

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

