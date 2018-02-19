from debian:buster

# Basic dependencies
run sed -i 's/main/main contrib non-free/g' /etc/apt/sources.list
run apt-get update
run apt-get install --no-install-recommends git build-essential -y
run apt-get install nvidia-cuda-dev nvidia-cuda-toolkit -y

# Adding gcc, gcc and g++ version 5. Builds fails with gcc-6 or higher.
run echo "deb http://ftp.ca.debian.org/debian/ sid main contrib non-free" >> /etc/apt/sources.list
run apt-get update
run apt-get install cmake g++-5 gcc-5 cpp-5 -y
run rm -fv /bin/cpp
run ln -vs /bin/cpp-5 /bin/cpp
run rm -fv /bin/gcc
run ln -vs /bin/gcc-5 /bin/gcc
run rm -fv /bin/g++
run ln -vs /bin/g++-5 /bin/g++

# This will keep the downloaded hunter dependencies if we want to build again. 
run ln -vs /ethminer/build/.hunter /root/.hunter

# Clone moste recent version of ethminer. 
run git clone https://github.com/ethereum-mining/ethminer.git

cmd cd /ethminer/build && cmake .. -DETHASHCUDA=ON -DETHASHCL=OFF -DETHSTRATUM=ON && cmake --build .
