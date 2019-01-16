# prediction-loc

#### Setup
* Install necessary libraries:  
`pip3 install --user boto3`  
`pip3 install --user gtfs-realtime-bindings`  
`pip3 install --user protobuf`

* Install and setup AWS authentication with `awscli`:  
`pip3 install --user awscli`  
`aws configure`  
Enter "Access Key ID" and "Secret Access Key" provided by an AWS administrator

* Ensure certificates are set up.  
If you're using macOS go to Macintosh HD > Applications > Python folder > double click on "Install Certificates.command" file.

* Configure  
`export S3_BUCKET_NAME=bucket-name`
Bucket name is shared on LastPass

#### Usage

`python3 getArchive.py --datetime [YYYY-MM-DDTHH:mm] --output [output file location]`

###### Optional arguments

|       Argument       |                            Description                             |
| -------------------- | ------------------------------------------------------------------ |
| `--stop [stop id]`   | Use to only include trip_updates affecting the given stop_id       |
| `--route [route id]` | Use to only include trip_updates affecting the given route         |
| `--feed [name]`      | Feed to retrieve. Accepted values: `bus` (default), `rtr`          |
| `--raw`              | Download the file as a raw protobuf instead of human-readable text |
