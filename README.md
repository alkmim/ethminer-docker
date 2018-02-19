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
2023 │ \  m  14:00:02|ethminer|  ethminer version 0.14.0.dev1                                                                          
2024 │   m  14:00:02|ethminer|  Build: Linux/g++ / Release                                                                             
2025 │  cu  14:00:02|ethminer|  Using grid size 8192 , block size 128                                                                  
2026 │ Benchmarking on platform: CUDA                                                                                                  
2027 │ Preparing DAG for block #0                                                                                                      
2028 │   ℹ  14:00:02|cuda-0  |  No work. Pause for 3 s.                                                                                
2029 │ Warming up...                                                                                                                   
2030 │   ℹ  14:00:05|cuda-0  |  Initialising miner 0                                                                                   
2031 │  cu  14:00:06|cuda-0  |  Using device: GeForce GTX 1070  (Compute 6.1)                                                          
2032 │  cu  14:00:06|cuda-0  |  Set Device to current                                                                                  
2033 │  cu  14:00:06|cuda-0  |  Resetting device                                                                                       
2034 │  cu  14:00:06|cuda-0  |  Allocating light with size: 16776896                                                                   
2035 │  cu  14:00:06|cuda-0  |  Generating mining buffers                                                                              
2036 │  cu  14:00:06|cuda-0  |  Generating DAG for GPU # 0  with dagSize: 1073739904  gridSize: 8192                                   
2037 │ Trial 1...                                                                                                                      
2038 │ 26122603                                                                                                                        
2039 │ Trial 2...                                                                                                                      
2040 │ 26017693                                                                                                                        
2041 │ Trial 3...                                                                                                                      
2042 │ 25917969                                                                                                                        
2043 │ Trial 4...                                                                                                                      
2044 │ 25917969                                                                                                                        
2045 │ Trial 5...                                                                                                                      
2046 │ 25917969                                                                                                                        
2047 │ min/mean/max: 25917969/25978840/26122603 H/s                                                                                    
2048 │ inner mean: 17380098 H/s 
```
