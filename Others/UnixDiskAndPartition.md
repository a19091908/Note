<h3>Disk And Partition</h3>

* Sector(磁區)
    - 512 bytes
    - 4K bytes    

<h4>MBR(Master Boot Record 主開機記錄)</h4>

* Contents Of MBR
    - Master Boot Record: 446 bytes
    - Partition table: 64 bytes (four 16 bytes)
    - End flags: 2 bytes

* Types of Partition
    - Primary
    - Extended
    - Logical

* Limitation
    - At most 1 extended partition.
    - The sum of primary and extended partitions is at most 4.
    - If you want more than 4 partitions, you should use an extended partition to separate it into lots of logical partitions.  

<h4>GPT(GUID partition Table)</h4>
GPT cannot be excuted by BIOS. Instead, it can be run by UEFI(Unified Extensible Firmware Interface).

* Contents Of GPT
    - LBA0 (MBR 相容區塊): 512 bytes
        + 446 bytes is similar to MBR
        + The rest of bytes contains a special flag which indicates the form of disk is GPT. 
    - LBA1 (GPT 表頭紀錄): 512 bytes
    - LBA2-33 (實際紀錄分割資訊處)

* All partitions are the primary partition.

* 開機的流程：BIOS --> MBR --> boot loader --> 核心檔案
