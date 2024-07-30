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

#The output should be as follows:

ubuntu@ip-xxxx:~/dill$ ./dill_validators_gen new-mnemonic --num_validators=1 --chain=andes --folder=./

***Using the tool on an offline and secure device is highly recommended to keep your mnemonic safe.***

Please choose your language ['1. العربية', '2. ελληνικά', '3. English', '4. Français', '5. Bahasa melayu', '6. Italiano', '7. 日本語', '8. 한국어', '9. Português do Brasil', '10. român', '11. Türkçe', '12. 简体中文']:  [English]: 3
Please choose the language of the mnemonic word list ['1. 简体中文', '2. 繁體中文', '3. čeština', '4. English', '5. Italiano', '6. 한국어', '7. Português', '8. Español']:  [english]: 4
Create a password that secures your validator keystore(s). You will need to re-enter this to decrypt them when you setup your Dill validators.:
Repeat your keystore password for confirmation:
The amount of DILL token to be deposited(2500 by default). [2500]:
This is your mnemonic (seed phrase). Write it down and store it safely. It is the ONLY way to retrieve your deposit.


Creating your keys.
Creating your keystores:	  [####################################]  1/1
Verifying your keystores:	  [####################################]  1/1
Verifying your deposits:	  [####################################]  1/1

Success!
Your keys can be found at: ./validator_keys


Press any key.
ubuntu@ip-xxxx:~/dill$

3-Import your keys to a keystore file With the following command:

./dill-node accounts import --andes --wallet-dir ./keystore --keys-dir validator_keys/ --accept-terms-of-use

#Check your validator keys With the following command:

ls -ltr ./validator_keys

4-Write the password you configured in the previous step into a file:

echo 123@dill > walletPw.txt
