# ethminer-docker
Allows you to build ethminer in a docker container. 

### Use

```
docker build -t ethminer-builder .
docker run -v $(pwd)/build:/ethminer/build ethminer-builder
```

### Testing ethminer binary

```
./build/ethminer/ethminer -U -M                                                           
\  m  14:00:02|ethminer|  ethminer version 0.14.0.dev1                                                                                 
  m  14:00:02|ethminer|  Build: Linux/g++ / Release                                                                                    
 cu  14:00:02|ethminer|  Using grid size 8192 , block size 128                                                                         
Benchmarking on platform: CUDA                                                                                                         
Preparing DAG for block #0                                                                                                             
  ℹ  14:00:02|cuda-0  |  No work. Pause for 3 s.                                                                                       
Warming up...                                                                                                                          
  ℹ  14:00:05|cuda-0  |  Initialising miner 0                                                                                          
 cu  14:00:06|cuda-0  |  Using device: GeForce GTX 1070  (Compute 6.1)                                                                 
 cu  14:00:06|cuda-0  |  Set Device to current                                                                                         
 cu  14:00:06|cuda-0  |  Resetting device                                                                                              
 cu  14:00:06|cuda-0  |  Allocating light with size: 16776896                                                                          
 cu  14:00:06|cuda-0  |  Generating mining buffers                                                                                     
 cu  14:00:06|cuda-0  |  Generating DAG for GPU # 0  with dagSize: 1073739904  gridSize: 8192                                          
Trial 1...                                                                                                                             
26122603                                                                                                                               
Trial 2...                                                                                                                             
26017693                                                                                                                               
Trial 3...                                                                                                                             
25917969                                                                                                                               
Trial 4...                                                                                                                             
25917969                                                                                                                               
Trial 5...                                                                                                                             
25917969                                                                                                                               
min/mean/max: 25917969/25978840/26122603 H/s                                                                                           
inner mean: 17380098 H/s
```
