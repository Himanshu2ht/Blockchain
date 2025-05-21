### Basics commands to install Golang and Fabric

```
sudo apt update
```
to update the system

```
sudo apt install golang-go
```
to install golang-go

```
sudo snap install docker
```
to install docker

```
sudo apt install git
```
to install git

```
git clone -b main https://github.com/hyperledger/fabric-samples.git
```
to install fabric-samples

```
sudo apt install curl
```
to install curl


```
cd fabric-samples
```
to get in fabric-samples

```
sudo bash
```


```
curl -sSL https://bit.ly/2ysbOFE | bash -s
```
to pull hyperledger docker images


```
cd test-network
```
to get into test-network

```
./network.sh
```
```
./network.sh up
```
to up the network

```
./network.sh createChannel
```
to create channel

```
./network.sh down
```
to down the network

```
wget https://dist.ipfs.tech/kubo/v0.32.1/kubo_v0.32.1_linux-amd64.tar.gz
```

![Screenshot from 2025-04-07 14-43-58](https://github.com/user-attachments/assets/b99efb83-0302-47a0-a23e-12c27ef90749)


### Install IPFS

```
tar -xvzf kubo_v0.32.1_linux-amd64.tar.gz
```
to use kubo
```
cd kubo
```
to get into kubo directory

```
sudo bash install.sh
```
to move to local bin

```
ipfs init
```
to initialise ipfs

```
ipfs daemon
```
to use daemon

![one](https://github.com/user-attachments/assets/28cf8c2c-f1d6-44f3-ade3-37cb24e5b492)


```
ipfs.log 2>&1 &
```
To run ipfs daemon in background

```
echo "Hello, IPFS!" > hello.txt
ipfs add hello.txt
ipfs cat <CID>
```
to add file

![two](https://github.com/user-attachments/assets/a3498732-e133-41c6-a4f2-7b1e21234150)

```
mkdir myfolder
echo "File 1 content" > myfolder/file1.txt
echo "File 2 content" > myfolder/file2.txt
ipfs add -r myfolder
```
to add a directory

![three](https://github.com/user-attachments/assets/4e0d51e5-ae0e-4034-b79d-fe3ac89a0666)


```
ps aux | grep ipfs
```
lists running processes

```
kill <PID>
```
to kill the process

## encrypting and decrypting
```
echo "Hello, bruh" > myfile.txt
ipfs add myfile.txt
openssl enc -aes-256-cbc -pbkdf2 -iter 100000 -salt -in myfile.txt -out myfile_encrypted.txt -pass pass:yourpassword
ipfs add myfile_encrypted.txt
cat myfile_encrypted.txt
openssl enc -d -aes-256-cbc -pbkdf2 -iter 100000 -in myfile_encrypted.txt -out decrypted_file.txt -pass pass:yourpassword
cat decrypted_file.txt
ipfs add decrypted_file.txt
```

![enc-dec](https://github.com/user-attachments/assets/293f1b3a-4ba4-4b35-8f04-d93fb9c9a6f7)


## to push video and audio

```
ipfs add <audio-path>
```
to add audio

![audio](https://github.com/user-attachments/assets/63297200-f2dd-48e0-ae29-a319240ec2d5)


```
ipfs add <video-path>
```
## Metamask

![Screenshot from 2025-04-07 14-48-24](https://github.com/user-attachments/assets/55bf0fd6-bbd2-4ded-bc99-8f79064f0469)


## Free Sepolia Faucet 0.05 with GCP-
![Screenshot from 2025-04-07 14-46-20](https://github.com/user-attachments/assets/3fdcab56-9bfa-4c28-a308-b6c9ef92b843)



# Writing solidity contact and deploing on our metamask account

### Visit remix ide website

#### Create a new file and write down your code

![Screenshot from 2025-05-18 13-05-25](https://github.com/user-attachments/assets/075644d0-d920-41f6-9402-281e4e8f3d39)


#### Now compile your code from 3rd option; we will see a green tick after successful compile

### Deploy on Metamask using fourth option

![Screenshot from 2025-05-18 13-06-58](https://github.com/user-attachments/assets/0a9fc539-1425-4f35-9648-e83c36d7e08d)


![Screenshot from 2025-05-18 13-07-47](https://github.com/user-attachments/assets/37836f1e-1af1-477f-a02d-d8f347d6dc68)


#### Check your metamsk, your contract should have been successfully deployed.

![Screenshot from 2025-05-18 13-08-40](https://github.com/user-attachments/assets/427f61ad-e169-418d-909d-9fdcd998fa10)


















