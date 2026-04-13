# Read me before use: 

# install web drivers:

check your google chrome version with the following command:

google-chrome --version

if it is present then use the version number to install the driver. 

wget https://chromedriver.storage.googleapis.com/104.0.5112.79 {#YOUR VERSION NUMBER}/chromedriver_linux64.zip
sudo cp chromedriver_linux64 /usr/local/bin

if you don't have the google chrome then use this commands: 

wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb
google-chrome --version
wget https://chromedriver.storage.googleapis.com/104.0.5112.79/chromedriver_linux64.zip
pwd
sudo cp chromedriver_linux64 /usr/local/bin

# install softwares:

sudo apt-get install cd-hit
sudo apt-get install ncbi-blast+


#running of program:

We have already provided the different databses in the software it-self, If you wnat to use custom dtabase then just paste the custom databse in it's respective folder, be sure to not to change the name!!!

For trial we have provided few samples in the samples direcotry!

After all the installation run the program the program will be in the dist directory using 

./TargetX


