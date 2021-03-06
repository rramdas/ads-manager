# ADS Manager

The **ADS Manager** simulates the process of a real time ads platform and some ways to process the data.

## Setup Steps
 1. Create the EC2 machine(s).
    * This project was tested on a EC2 **Ubuntu Server 14.04 LTS (HVM), SSD Volume Type - ami-f0b11187** machine with an instance type **m3.large** with all the default options.

 2. Connect to the created machine
    * ssh -i mykey.pem ubuntu@mypublicdns

 3. Download the install.sh file on the AdsManager public github repo
    under the prerequisites folder.
    * curl -L -O https://raw.githubusercontent.com/miguelangcosta/ads-manager/master/prerequisites/install.sh

 4. Run the previous downloaded file on the EC2 machine. This will install all that is needed for this project to run.
    *   sh install.sh
 5. Fill the file ~/.aws/credentials with your correct aws keys.

## Run the Producer
    See ads-manager-kinesis-producer/README.md

## Run the Consumer
    See ads-manager-kinesis-consumrer/README.md

## Run the Aggregator
    See ads-manager-aggregator/README.md

## Notes
   The Producer, Consumer and Aggregator can run on different machines.

## Stop the applications
   * On AWS console go to Kinesis and delete the stream created
   * On AWS console go to DynamoDB and delete the table that have the application name of the ads-manager-kinesis-consummer



