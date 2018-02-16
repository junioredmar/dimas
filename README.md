# dimas
Project .NET Core deployed to AWS Beanstalk

# AWS Environment
https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/dotnet-core-tutorial.html
https://console.aws.amazon.com/elasticbeanstalk/home?region=us-east-1#/environment/dashboard?applicationName=dimas&environmentId=e-xihycwhm3w

# REGION EC2:
us-east-1a

# REGION RDS:
us-east-1a
us-east-1b

# SUB-NET:
subnet-e992af8d (172.31.0.0/20)
subnet-f8bff7d7 (172.31.80.0/20)

# EC2 Dimas ENVIRONEMNT
dimas-env.us-east-1.elasticbeanstalk.com

# BUILD:
dotnet publish -o site
cd .\site\
zip ../site.zip *
cd ..
zip dotnet-core-tutorial.zip site.zip aws-windows-deployment-manifest.json
