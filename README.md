

	____ ____ _    ____ ____ ____ ____ ____ __   
	| __\| . \||_/\| . \|_ _\|   ||  _\| __\| \|\
	| \__|  <_| __/| __/  || | . || [ \|  ]_|  \|
	|___/|/\_/|/   |/     |/ |___/|___/|___/|/\_/



GenMiner's CryptoGen nVidia GPU Miner.
=====================================

Some say "The best mining software for nVidia GPUs". I just say : "Make your own opinion".

Latest version is v3.0.2

DOWNLOAD :
--------
* Windows : <https://github.com/genminer/cryptogen/releases>
* Linux :   not yet


HARDWARE / SYSTEM NEEDED :
------------------------
- OS : Windows 10 x64 (pro or enterprise recommended)
- GPUs : 98x / 10xx cards (1080ti 8GB+ recommended :-)
- Recent nVidia drivers (ex: 397.64), with compute capability 5.0 and beyond.


FEATURES :
--------
- Built for nVidia with CUDA 9.0, 32bits version (anyway faster than 64bits version)
- New optimized code with special portions. Effective hashrate is higher, without power overkill.
- Up to 16 GPUs can be used.
- Supports Stratum versions
- Shows detailed mining information and hashrate for each card.

SPECIAL FEATURES :
----------------
- Supplied batch file allows easier choice for mining.
- You may create configuration files with pools, one file for each coin. Much simple to manage.
- Up to 16 pools in each configuration file.
- Automatic watchdog, auto-terminate if too many errors occurs (--max-rejects, default=7)
- Inactivity watchdog, auto-terminate if program stucks more than 120s.
- Automatic failover to next pool if current doesn't work.
- Miner can be restarted if too many blocks pass without submission (-M, --max-blocks-null)
- Special parameters can be used in the configuration file / pools zone (%WORKER%, %DIFF%)


INSTALLATION GUIDE : 
--------------------
- Unzip downloaded file into desired folder
- Update cryptogen.*.conf files with your own information (pools, wallet addresses, etc)
- Feel free to add new pools in .conf files
- Feel free to add new conf files for your preferred coins.
- Update file CRYPTOGEN-MINE.bat to choose coin to mine.
- Execute (double-click) CRYPTOGEN-MINE.bat


CONFIGURATION FILES :
-------------------
The batch file CRYPTOGEN-MINE.bat uses one configuration file for each coin to mine.    
These files must be in JSON format, some are provided as examples.    
Some options (like -w or -z) define "tags" values usable in config file.


FREE SOFTWARE :
-------------
Using this software is free, however, a default developer fee of 2% is applied. During each cycle of 6000 seconds (100 minutes), 
the software will mine 120s for the developer. One don't know in advance when the developer mining will occur during the cycle.    
You can reduce the fee, anyway your contribution is highly appreciated. If you don't agree with this, don't use this software.


COMMAND LINE OPTIONS :
--------------------
```
  -a, --algo=ALGO        Specify the algorithm to use
             bastion     Hefty bastion
             bitcore     Timetravel-10
             blake       Blake256-14rounds(SFR)
             blake2s      Blake2s          (NEVA/XVG/XSH)
             blakecoin   Blake256-8rounds (BLC)
             bmw         BMW 256
             cryptolight AEON cryptonight(MEM / 2)
             cryptonight XMR cryptonight
             c11         C11/flax         (AXS/CHC/SPD/IMC/JLG/DXC/ANU)
             decred      Blake256-14rounds(DCR)
             deep        Deepcoin
             dmd-gr      Diamond - Groestl
             equihash    Zcash Equihash
             fresh       Freshcoin(shavite 80)
             fugue256    Fuguecoin
             groestl     Groestlcoin
             hmq1725     Doubloons/Espers
             hsr         X13+SM3          (Hshare)
             jackpot     JHA v8
             keccak      keccak256        (Maxcoin)
             keccakc     Keccak - 256 (CreativeCoin)
             lbry        Lbry             (Library Credits)
             luffa       Joincoin
             lyra2       CryptoCoin
             lyra2v2     VertCoin
             lyra2z      ZeroCoin(3rd impl)
             myr-gr      Myriad-Groestl   (SFR/AUR/DGB/XVG/MYR)
             neoscrypt   Neoscrypt        (FTC/PXC/UFO)
             nist5       NIST5            (Talkcoin/Power)
             penta       Pentablake hash(5x Blake 512)
             phi         PHI1612          (LUX/FLM/SERA)
             phi2        PHI v2           (LUX since block 300K)
             polytimos   Politimos
             quark       Quark            (Quarkcoin)
             qubit       Qubit
             sha256d     SHA256d          (bitcoin)
             sha256t     SHA256 x3
             sia         Sia              (SIAcoin)
             sib         X11+gost         (Sibcoin)
             scrypt      Scrypt
             scrypt-jane Scrypt-jane Chacha
             skein       Skein SHA2       (AUR/DGB/SKC)
             skein2      Double Skein     (Woodcoin)
             vcash       Blake256-8rounds (XVC)
             skunk       Skein Cube Fugue Streebog
             s3          S3               (1Coin)
             timetravel  Machinecoin permuted x8
             tribus      Denarius
             vanilla     Blake256-8       (VNL)
             veltor      Thorsriddle streebog
             whirlcoin   Old Whirlcoin    (Whirlpool algo)
             whirlpool   Whirlpool        (JoinCoin)
             x11         X11              (DarkCoin)
             x11evo      Permuted x11     (Revolver)
             x12         X12              (GalaxyCash)
             x13         X13              (MaruCoin)
             x14         X14              (BernCoin)
             x15         X15              (Joincoin)
             x15         X15
             x16r        X16R             (Raven)
             x16s        X16S
             x17         X17              (XVG)
             wildkeccak  Boolberry
             zr5         ZR5              (ZiftrCoin)
      --api-remote       Allow remote control, like pool switching
  -b, --api-bind=port    IP:port for the miner API (ex: 127.0.0.1:4068), 
                         0=disabled (default disabled) 
  -B, --background       Run the miner in the background
      --benchmark        Run in offline benchmark mode
      --cert=FILE        Certificate for mining server using SSL
  -c, --config=FILE      Load a JSON-format configuration file
      --cputest          Debug hashes from cpu algorithms
      --cpu-affinity     Set process affinity to cpu core(s), mask 0x3 for cores 0 and 1
      --cpu-priority     Set process priority (default: 3) 0 idle, 2 normal to 5 highest
      --cuda-schedule    Set device threads scheduling mode (default: auto)
  -D, --debug            Enable debug output
  -d, --devices          Comma separated list of CUDA devices to use.
                         Device IDs start counting from 0!Alternatively takes
                         string names of your cards like gtx780ti or gt640#2
                         (matching 2nd gt640 in the PC)
  -f, --diff-factor      Divide difficulty by this factor (default 1.0)
      --donate           Percentage of time to donate to the developer
  -h, --help             Display this help text and exit
  -i, --intensity=N[,N]  GPU intensity 8.0-25.0 (default: auto)
                         Decimals are allowed for fine tuning
  -m, --diff-multiplier  Multiply difficulty by this value (default 1.0)
  -M, --max-blocks-null  Maximum quantity of blocks without submit (default no limit)
      --max-rejects      Maximum quantity of rejected blocks before terminating.
                         (value between 3 and 32, default=7)
      --max-temp=N       Only mine if gpu temp is less than specified value
      --max-rate=N[KMG]  Only mine if net hashrate is less than specified value
      --max-diff=N       Only mine if net difficulty is less than specified value
                         Can be tuned with --resume-diff=N to set a resume value
  -n, --ndevs            List cuda devices
  -N, --statsavg         Number of samples used to compute hashrate (default: 30)
      --no-color         Disable colored output
      --no-extranonce    Disable extranonce subscribe on stratum
      --no-gbt           Disable getblocktemplate support (height check in solo)
      --no-longpoll      Disable X-Long-Polling support
      --no-stratum       Disable X-Stratum support
  -o, --url=URL          URL of mining server
  -O, --userpass=U:P     username:password pair for mining server
  -p, --pass=PASSWORD    Password for mining server
  -P, --protocol-dump    Verbose dump of protocol-level activities
  -q, --quiet            Disable per-thread hashmeter output
  -R, --retry-pause=N    Time to pause between retries, in seconds (default: 30)
  -r, --retries=N        Number of times to retry if a network call fails
                         (default: retry indefinitely)
  -s, --scantime=N       Upper bound on time spent scanning current work when
                         long polling is unavailable, in seconds (default: 60)
  -T, --timeout=N        Network timeout, in seconds (default: 300)
  -t, --threads=N        Number of miner threads (default: number of nVidia GPUs)
      --time-limit       Maximum time [s] to mine before exiting the program.
      --trust-pool       Trust the max block reward vote (maxvote) sent by the pool
  -u, --user=USERNAME    Username for mining server
      --vote=VOTE        Vote (for decred and HeavyCoin)
  -V, --version          Display version information and exit
  -x, --proxy=[PROTOCOL://]HOST[:PORT]  Connect through a proxy
  -z, --diff=0.0         Set wanted difficulty, to be used in pool file as DIFF
                         When reach, end program
      --watch-timeout    Timeout in seconds for inactivity. Value between 30 and 3600,
                         default=120, 0 to disable inactivity watchdog.
      --watch-quiet      Dont display watchdog living messages
  -w, --worker=name      Set worker name, to be used in pool file as WORKER
GPUs options :
      --mem-clock=3505   Set the gpu memory boost clock
      --gpu-clock=1150   Set the gpu engine boost clock
      --plimit=100       Set the gpu power limit in percentage
      --tlimit=80        Set the gpu thermal limit in degrees
      --led=100          Set the logo led level (0=disable, 0xFF00FF for RVB)

```

<<< THIS PROGRAMM IS PROVIDED "AS-IS", USE IT AT YOUR OWN RISK ! >>>

