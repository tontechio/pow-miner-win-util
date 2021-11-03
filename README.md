# README

Windows utils for https://github.com/tontechio/pow-miner-gpu

## Batch files

Requirements: you must have miner binaries in your system, see https://github.com/tontechio/pow-miner-gpu

- `run_config.ini` - miner and tools configuration
- `test_cuda.bat` - run performance test for Nvidia GPU
- `run_cuda.bat` - run miner for Nvidia GPU
- `test_opencl.bat` - run performance test for AMD GPU
- `run_opencl.bat` - run miner for Nvidia GPU

### Usage

1. Download, extract and place to same directory where miner `*.exe` files located
2. Edit `run_config.ini`, variable names self-explanatory
3. Run `test_cuda.bat` or `test_opencl.bat` (based on your GPU) for performance test and optimal BOOST_FACTOR value
4. Do not forget to enable (`USE_LOG=Y`) or disable (`USE_LOG=N`) miner logging
5. Run `run_cuda.bat` or `run_opencl.bat` (based on your GPU) to start the miner

