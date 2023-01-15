# マルチモーダル情報を扱う世界モデル

## Ominicampusでの実験の回し方

Ominicampusの実験環境は利用上限が100時間までと決まっているため, 利用完了したらすぐにインスタンスを削除する必要があります.
`/mnt/shared` はAWS S3へマウントしているためここに保存したデータは永続化しますが, それ以外のデータはインスタンス削除とともに削除されてしまいます.

Ominicampusの利用が必要なとき(GPUが必要なとき)はJupiterHubにログイン後以下のコマンドを叩いてレポジトリをクローンしてください.
GitHubとの連携に必要なsshの設定を`/mnt/shared`からホームディレクトリにコピーしてくることができます.

```
$ cd ~
$ cp -r /mnt/shared/.ssh ~/
$ chmod 600 /home/admin/.ssh/id_rsa
$ git clone git@github.com:meltyyyyy/multimodal-world-model.git
```

## Omnicampus環境

```
$ cat /etc/os-release
NAME="Ubuntu"
VERSION="20.04.5 LTS (Focal Fossa)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 20.04.5 LTS"
VERSION_ID="20.04"
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
VERSION_CODENAME=focal
UBUNTU_CODENAME=focal
```

```
$ lscpu
Architecture:                    x86_64
CPU op-mode(s):                  32-bit, 64-bit
Byte Order:                      Little Endian
Address sizes:                   48 bits physical, 48 bits virtual
CPU(s):                          16
On-line CPU(s) list:             0-15
Thread(s) per core:              2
Core(s) per socket:              8
Socket(s):                       1
NUMA node(s):                    1
Vendor ID:                       AuthenticAMD
CPU family:                      23
Model:                           49
Model name:                      AMD EPYC 7R32
Stepping:                        0
CPU MHz:                         2613.422
BogoMIPS:                        5599.34
Hypervisor vendor:               KVM
Virtualization type:             full
L1d cache:                       256 KiB
L1i cache:                       256 KiB
L2 cache:                        4 MiB
L3 cache:                        32 MiB
NUMA node0 CPU(s):               0-15
```

```
$ nvidia-smi
Sun Jan 15 07:37:34 2023       
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 525.60.11    Driver Version: 525.60.11    CUDA Version: 12.0     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  NVIDIA A10G         Off  | 00000000:00:1E.0 Off |                    0 |
|  0%   17C    P8     9W / 300W |      0MiB / 23028MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
                                                                               
+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
|  No running processes found                                                 |
+-----------------------------------------------------------------------------+
```

## メンバー

ここにぞれぞれ自己紹介をどうぞ

