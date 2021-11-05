# README

Windows utils for https://github.com/tontechio/pow-miner-gpu

## Batch files

Requirements: you must have miner binaries in your system, see https://github.com/tontechio/pow-miner-gpu

- `run_config.ini` - miner and tools configuration
- `test_cuda.bat` - run performance test for Nvidia GPU
- `run_cuda.bat` - run miner for Nvidia GPU
- `test_opencl.bat` - run performance test for AMD GPU
- `run_opencl.bat` - run miner for AMD GPU

### Usage

1. Download, extract and place to same directory where miner `*.exe` files located
2. Edit `run_config.ini`, variable names self-explanatory
3. Run `test_cuda.bat` or `test_opencl.bat` (based on your GPU) for performance test and optimal BOOST_FACTOR value
4. Do not forget to enable (`USE_LOG=Y`) or disable (`USE_LOG=N`) miner logging
5. Run `run_cuda.bat` or `run_opencl.bat` (based on your GPU) to start the miner

### run_config.ini

- `GIVER_ADDR`: one of giver-contract address, choose one from [https://ton.org/mining](https://ton.org/mining)
- `MY_ADDR`: your personal wallet address, get wallet app from [https://ton.org/wallets](https://ton.org/wallets) and create a wallet
- `GPU_ID`: your GPU for multi-gpu systems. First GPU comes with `GPU_ID=0`, second with `GPU_ID=1`, etc
- `GPU_PLATFORM_ID`: this is related to OpenCL (AMD) only. Check your driver stats and/or dry-run the miner - it will show which platform number and gpu id is available
- `BOOST_FACTOR`: mining perfomance tuning for your setup. Run `test_cuda.bat` or `test_opencl.bat` to get optimal `BOOST_FACTOR` value
- `CONFIG_FILE`: TON network config file [https://newton-blockchain.github.io/global.config.json](https://newton-blockchain.github.io/global.config.json)
- `USE_LOG`: value `Y` enable logging. Value `N` disable logging
- `LOG_FILE`: filename used when `USE_LOG=Y`
- `TEST_TIME`: time in seconds for each test in `test_cuda.bat` or `test_opencl.bat` to obtain `BOOST_FACTOR` value. Lower to get faster results, rise to get more accurate results





