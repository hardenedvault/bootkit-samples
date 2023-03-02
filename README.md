# Bootkit samples
Bootkit sample from real-life attack. Be careful about tweaking the sample for research purpose. 

Password: danger

## Bootkits has been found in the wild

| Malware/Bootkits | Disclosure date | 1st blood   | Infection type |Targeted OS | Malware “vendor” |
|:--------------------:|:-----------------:|:-------------:|:----------:|:-------------------:|:--------:|
|[Vector-EDK (Leaked source code)](https://github.com/hackedteam/vector-edk) |2015 |2014 |DXE |? |HackingTeam |
|[DerStarke](https://wikileaks.org/ciav7p1/cms/page_3375125.html) |2016 |2013? |DXE |Windows/Linux/MacOS | Vault7 |
|[QuarkMatter](https://wikileaks.org/ciav7p1/cms/page_21561431.html) |2016 |2013? |ESP |Windows/Linux | Vault7 |
|[LoJaX](https://www.eset.com/fileadmin/ESET/US/resources/datasheets/ESETus-datasheet-lojax.pdf) |2018 |2017 or earlier |DXE | Windows  | APT28 |
|[TrickBot/TrickBoot](https://eclypsium.com/2020/12/03/trickbot-now-offers-trickboot-persist-brick-profit/) |2020 |2017 |DXE |Windows |N/A |
|[FinSpy](https://securelist.com/finspy-unseen-findings/104322/) |2021 |2011 |MBR/ESP |Windows/Linux/MacOS |N/A |
|[ESPecter](https://www.welivesecurity.com/2021/10/05/uefi-threats-moving-esp-introducing-especter-bootkit/) |2021 |2012/2020 |MBR/ESP |Windows |N/A |
|[Rovnix (Leaked source code)](https://github.com/m0n0ph1/Win64-Rovnix-VBR-Bootkit) |2011 |? |MBR/VBR |Windows |N/A |
|[MosaicRegressor](https://securelist.com/mosaicregressor/98849/) |2020 |? |DXE |Windows |N/A |
|[Implant.ARM.iLOBleed.a](https://threats.amnpardaz.com/en/2021/12/28/implant-arm-ilobleed-a/) | 2021 | ? | BMC | Linux | N/A |
|[MoonBounce](https://securelist.com/moonbounce-the-dark-side-of-uefi-firmware/105468/) based on Vector-EDK | 2021 | ? | DXE | Windows | APT41 |
| [Conti leaked chat](https://github.com/hardenedvault/bootkit-samples/blob/master/osint/conti_leaked_chat.md) | 2021 | ? | CSME via undocumented HECI, SMM | Windows/Linux/? | Conti group |
| [BlackLotus](https://www.welivesecurity.com/2023/03/01/blacklotus-uefi-bootkit-myth-confirmed/) | [2022](https://www.bleepingcomputer.com/news/security/malware-dev-claims-to-sell-new-blacklotus-windows-uefi-bootkit/) | 2022 | ESP | Windows | N/A |

## Massive exploitation
| Vulnerability | Target |
|:--------------------:|:-----------------:|
|[CVE-2022-21894](https://github.com/Wack0/CVE-2022-21894)| UEFI Secure Boot |



## Threat model - "Know your enemy"

HardenedVault is mainly focus on figuring out the infection stage of bootkits, which is crucial to work on security features for defense in [VaultBoot](https://github.com/hardenedvault/vaultboot). A typical malicious firmware may check if the security protections are set and implant (write) the bootkits into SPI flash if they're not set correctly (e.g. Write protection is not set, etc). If security protections are set properly, malicious firmware might achieve the persistent by utilizing exploits (e.g. CVE-2014-8273). Bootkits usually targeted MBR/ESP in the early 2010s, but as the cost of firmware attack decreased rapidly, the modern bootkits started to target DXE or even PEI.

![1](pic/fw-threat-model.png)


## Reference

* [What every CISO and security engineer should know about Intel CSME - 202107](https://hardenedvault.net/blog/2021-07-16-ciso-seceng_csme/)
* [CSME security](https://github.com/hardenedlinux/firmware-anatomy/blob/master/hack_ME/me_info.md)
* [UEFI/SMM security](https://github.com/hardenedlinux/firmware-anatomy/blob/master/hack_ME/firmware_security.md)

