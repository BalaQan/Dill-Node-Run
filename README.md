# Dill-Node-Run

Before starting, you need to get the Andes role in Discord, for this, go to the link below and do the tasks and wait until you get the role.

 https://app.galxe.com/quest/Dill/GCVWntghfL

 *After chosen you can start it

  #System Requirements (Minimum-Recommended):
  RAM 2GB  	CPU 2Core  	DISK 20-40GB SSD

  #Enter the following commands to update your server:

  sudo apt update && apt upgrade -y
  sudo apt install curl make wget clang net-tools pkg-config libssl-dev build-essential jq lz4 gcc unzip snapd -y

#Node installation steps:

1-Download Binaries with the following command:

  cd $HOME && curl -O https://dill-release.s3.ap-southeast-1.amazonaws.com/linux/dill.tar.gz && \
  tar -xzvf dill.tar.gz && cd dill

2-Generate Validator Keys With the following command:

  ./dill_validators_gen new-mnemonic --num_validators=1 --chain=andes --folder=./
