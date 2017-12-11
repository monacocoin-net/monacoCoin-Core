# monacoCoin-Core

MonacoCoin Projet : Please use the new version : https://github.com/monacocoin-net/monoeci-core/releases

----------------------

How to update to Monoeci (Server and Wallet) : 
----------------------

Save your wallet and your config files : 

On linux : /home/YOUR NAME/.monacoCoinCore/

On Windows : C:\Users\YOUR NAME\AppData\Roaming\MonacoCoinCore\

On MacOs : /Users/sebastien/Library/Application\ Support/monacoCoinCore/

If you have doubts, back up the whole directory!
----------------------

1. Close your apps

2. Download the last version of Monoeci (cli ou wallet is the same) https://github.com/monacocoin-net/monoeci-core/releases

3. Open Wallet or monoecid , wait 1 minute and close

4. Go to monoeci folder :

On linux : /home/YOUR NAME/.monoeciCore/

On Windows : C:\Users\YOUR NAME\AppData\Roaming\monoeciCore\

On MacOs : /Users/YOURUSER/Library/Application\ Support/monoeciCore/

And copy paste wallet.dat and masternode.conf which come from your MonacoCoin Core directory
Copy and paste monacoCoin.conf and rename to monoeci.conf

5. Restart your server and wait for the full sync

For linux server (Masternode): 
----------------------

Connect with the same user who is running monacoCoinCore

```
  cd
  
  ./monacoCoin-cli stop
  
  tar zcvf save.tar.gz .monacoCoinCore/
  
  rm -fr sentinel
  
  wget https://github.com/monacocoin-net/monoeci-core/releases/download/0.12.2/monoeciCore-0.12.2-linux64-cli.taz.gz
  
  tar xvf monoeciCore-0.12.2-linux64-cli.taz.gz
  
  ./monoecid
  
```
Wait 1 minutes (directory and wallet are being created) for force to close process CTRL+C and wait !

```
cp .monacoCoinCore/wallet.dat .monoeciCore/

cp .monacoCoinCore/masternode.conf .monoeciCore/

cp .monacoCoinCore/monacoCoin.conf .monoeciCore/monoeci.conf

git clone https://github.com/monacocoin-net/sentinel.git 

cd sentinel/

virtualenv ./venv

./venv/bin/pip install -r requirements.txt

cd ..

./monoecid

```

now wait full sync and if you have masternode use : 

```

./monoeci-cli masternode start

```





  



  







