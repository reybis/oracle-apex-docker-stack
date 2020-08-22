# Oracle APEX Docker Compose Stack

[![APEX Community](https://cdn.rawgit.com/Dani3lSun/apex-github-badges/78c5adbe/badges/apex-community-badge.svg)](https://github.com/Dani3lSun/apex-github-badges) 
[![APEX 18.1](https://cdn.rawgit.com/Dani3lSun/apex-github-badges/2fee47b7/badges/apex-18_1-badge.svg)](https://github.com/Dani3lSun/apex-github-badges)
[![APEX 18.2](https://cdn.rawgit.com/Dani3lSun/apex-github-badges/2fee47b7/badges/apex-18_2-badge.svg)](https://github.com/Dani3lSun/apex-github-badges)
[![APEX 19.1](https://img.shields.io/badge/APEX-19.1-blue.svg?style=flat&logo=data%3Aimage%2Fpng%3Bbase64%2CiVBORw0KGgoAAAANSUhEUgAAADwAAAA7CAQAAACN8CFBAAAHHUlEQVRYw%2B1ZaUxUVxQGq4g1qNVqW0M0qXWLiqmWRHDp2KCZH9CqUWPEbVqxVJS21lQndYmaGiBAAXEBEcEAMVSUsAwwzIADwyo7CAgIqKyyzsIMs96q%2BN65784bGZB%2F9f5795xzv3vPOfcs91lZfRhvxrbVKU4ZTt5r3m%2BVA4uvOd1yOu%2B0dZZF7KfnPyvTodfDgGStSV%2BPBzJ4VnbWYO%2FIKgjJUefT2ydHEQlfM5iJsNHbI3QaK2yAU3MtIoYG1d0%2BOcOsSNTy9mpSpL83Y9WYTrvqaS9iHY9C19myity1HXrGJqBSCudZChs0r0sJkgakRUZspZC9LCIxnw11A0tjS246fKlVQgdLYH0delQg9aIpYWvi0uAAUEBepYlI4lfGBhB53By2INq2%2FqqBnhnoF24aDdZ%2F0%2FN%2BWKOo6doXI%2FOitT3UVhBnGiFUmQQiTS3hc1%2FPxU9ujtaDrftEzu%2BCDXRu7aN4jaimLtQOaFIxNe9hzxBymwVbbWnAKS1RAK2QixaZte2iDjkGW8Okiu5QNG8m8Hl7OG3EFJwSb%2F3kCuhCr09dxgZ7eZkc9ocKGoMnM%2BlVYormyQTm0cBqFBXNFLo%2FtcEPPFMpT%2BeYwHK65AArqQ%2F6lLikocPUsZALsSWrato%2BQyjyFseGAT2lMRQONNifsYUBu6WtH5ScXxfwCXPl0oNa2tML0kyUJd6jBoWi6BAOcdVbwwC6owfmfRw7ZQBbXkauW7fbSF8NOfJ1YbFTAg8zE4q%2F4fIRk%2F40dEThOn3oKWru6gqZFmTyq8k1H7tj%2FoFEPFa%2F5E%2BK2jNMs2mR6C6TfsI25d5ryr%2BedEz%2Bth8EkLA20I4pUeGl00KsFu8Jm2T2Lgo9lVhYF8W7MDw8ySY5Ic2d%2BvJz7cCUnFlL2rbiuFYNLvvIc5To89BrCFOO8BZ3GjufzxbctkXFAcRpangGHcCWelkQb1N4mP5QZgR3qilPiOOAGmALi01ciocwo0l5FmYYf1cNgmXFCSaw61VYyhHUkKet8IaUpEX3XC3OqHzrB%2B5KbMeSFFds6ZBtPUOwreSqQCK9V5zSaSAm5LuHWY%2BpihAfVtDQMk38dDomb%2B%2BUQ7YVFfoQhqj01msBtuzwOOqm9IMjB1OqIo%2FSsJxeFcBKckiZek8sh6PCg%2BOsEm%2B6DRu0unB619c5w5jtU4pI%2FupfsRrLkOQ27vKUbx3oFkCnhMDtMg3AxpZfJC5axTm4QCqU7BZrbTURI2jvSyUoObHwwscE7BmIUkpU5D5BBX4w5sl6lCUm6U9%2BNxoBtmTfBMFGcIcMcNr0LJJe%2Bwdca7VB9MMEwV7ehkeyqFKSXnQJg0VhGyYI1ocHwdGAIovPEi5V7KvXgZLFE3Va3wN9mG2TMkwu0FkDbQQFKtxNx%2FvFcQfeAzZsh0ILsAKBiUvxQclDKI8%2Bbf6S7jadVrJjnLA3duLhIjabpFdhtlVpY%2Bmau3hOf%2BfIbPbO8dj2sFIHsAGFfBsmvTAElKxEqd%2FRSp42%2BJKa1%2BlSxxqr%2Fz46oAIl30k%2FSdRfJX4GPdhW%2Bj1WpVgnBGiwnktwdAywiUsGNAB7%2F4FJmr8A10uJpCb5NjkEjKTRiCx1s%2BCFbVibGZNM0isuYy41nMTaytX%2BghWfr3KyBbAe1slVAOuTS9Jzr2NdhTHW0dw6kp14sSz0GBX4%2Fi4t7VKCjDNTiOXC9fR6MiShy%2FPTXHGxqx2z5yrahytccGIU4Pp8irmm3kTJ%2FnBaOcrj0kFzzcArTxbncGcT1cjP0KVrhlOPvQP2EIeqWQeQP6HGarx10who2%2BY59HWNzGZlc4mHpTIPaIyMRqn5yxUnodhy45mUR9cAVqEOw17AumuwYriCS%2FRc0t1arCJN%2B8kMcF8zxXKJEfCK4yBcDKLEdYzHpXWd2C1I6%2BBOx6mx1hmucOoGDSvsrhVUkVHSCN3i6cVl5dhbCMrdbKKnze1YcM0sJ21dsF9JU8%2FYswDfbjC%2B3XfQW%2Ffnzs%2Fmd%2FaAqmQG8Ua2Ld%2FZ2AV7Q9lSlzk4dcPc2iaK5mcKfGzh4Fth%2BfCfr3r65JWSv7o1%2BHuXTBFm9tGJ7%2FASCnEkKnWhy%2FwNM8W10Bwc%2Bdz0yq%2BnvCBc4OVc1E4%2Bs3XrL7zzrYvv0InFjNRu1zfloOuMVOzlq%2FwJi2CylLKDXKE3kLAFDXcXjBZ8Ip1eYG4maOHM5swVPQenfob81poInfuyi%2F0B8tVGXshyvH6baUmcj3Fuw2N0SX4l9s5nCF%2FLIpLDYwPtRh0PM86NKY%2Bv7pSzrdTed3wpq0BxLpNRrWlvvxlxxG4c%2FcfKDgUJ2yY7voz9Rd6uB1Ntlz7mSs7MH23GW6v5OzxnwLai88vNsF60H8lJDeihv%2Fg9fwi8aQEc6dyKqlHoarOMLjbCs%2BX80m%2F221hN0IiyiTsk%2BScn4MH%2Be5M%2B%2FOP5f47%2FABRC7md%2F2UDNAAAAAElFTkSuQmCC)](https://github.com/Dani3lSun/apex-github-badges)
[![APEX 19.2](https://img.shields.io/badge/APEX-19.2-blue.svg?style=flat&logo=data%3Aimage%2Fpng%3Bbase64%2CiVBORw0KGgoAAAANSUhEUgAAADwAAAA7CAQAAACN8CFBAAAHHUlEQVRYw%2B1ZaUxUVxQGq4g1qNVqW0M0qXWLiqmWRHDp2KCZH9CqUWPEbVqxVJS21lQndYmaGiBAAXEBEcEAMVSUsAwwzIADwyo7CAgIqKyyzsIMs96q%2BN65784bGZB%2F9f5795xzv3vPOfcs91lZfRhvxrbVKU4ZTt5r3m%2BVA4uvOd1yOu%2B0dZZF7KfnPyvTodfDgGStSV%2BPBzJ4VnbWYO%2FIKgjJUefT2ydHEQlfM5iJsNHbI3QaK2yAU3MtIoYG1d0%2BOcOsSNTy9mpSpL83Y9WYTrvqaS9iHY9C19myity1HXrGJqBSCudZChs0r0sJkgakRUZspZC9LCIxnw11A0tjS246fKlVQgdLYH0delQg9aIpYWvi0uAAUEBepYlI4lfGBhB53By2INq2%2FqqBnhnoF24aDdZ%2F0%2FN%2BWKOo6doXI%2FOitT3UVhBnGiFUmQQiTS3hc1%2FPxU9ujtaDrftEzu%2BCDXRu7aN4jaimLtQOaFIxNe9hzxBymwVbbWnAKS1RAK2QixaZte2iDjkGW8Okiu5QNG8m8Hl7OG3EFJwSb%2F3kCuhCr09dxgZ7eZkc9ocKGoMnM%2BlVYormyQTm0cBqFBXNFLo%2FtcEPPFMpT%2BeYwHK65AArqQ%2F6lLikocPUsZALsSWrato%2BQyjyFseGAT2lMRQONNifsYUBu6WtH5ScXxfwCXPl0oNa2tML0kyUJd6jBoWi6BAOcdVbwwC6owfmfRw7ZQBbXkauW7fbSF8NOfJ1YbFTAg8zE4q%2F4fIRk%2F40dEThOn3oKWru6gqZFmTyq8k1H7tj%2FoFEPFa%2F5E%2BK2jNMs2mR6C6TfsI25d5ryr%2BedEz%2Bth8EkLA20I4pUeGl00KsFu8Jm2T2Lgo9lVhYF8W7MDw8ySY5Ic2d%2BvJz7cCUnFlL2rbiuFYNLvvIc5To89BrCFOO8BZ3GjufzxbctkXFAcRpangGHcCWelkQb1N4mP5QZgR3qilPiOOAGmALi01ciocwo0l5FmYYf1cNgmXFCSaw61VYyhHUkKet8IaUpEX3XC3OqHzrB%2B5KbMeSFFds6ZBtPUOwreSqQCK9V5zSaSAm5LuHWY%2BpihAfVtDQMk38dDomb%2B%2BUQ7YVFfoQhqj01msBtuzwOOqm9IMjB1OqIo%2FSsJxeFcBKckiZek8sh6PCg%2BOsEm%2B6DRu0unB619c5w5jtU4pI%2FupfsRrLkOQ27vKUbx3oFkCnhMDtMg3AxpZfJC5axTm4QCqU7BZrbTURI2jvSyUoObHwwscE7BmIUkpU5D5BBX4w5sl6lCUm6U9%2BNxoBtmTfBMFGcIcMcNr0LJJe%2Bwdca7VB9MMEwV7ehkeyqFKSXnQJg0VhGyYI1ocHwdGAIovPEi5V7KvXgZLFE3Va3wN9mG2TMkwu0FkDbQQFKtxNx%2FvFcQfeAzZsh0ILsAKBiUvxQclDKI8%2Bbf6S7jadVrJjnLA3duLhIjabpFdhtlVpY%2Bmau3hOf%2BfIbPbO8dj2sFIHsAGFfBsmvTAElKxEqd%2FRSp42%2BJKa1%2BlSxxqr%2Fz46oAIl30k%2FSdRfJX4GPdhW%2Bj1WpVgnBGiwnktwdAywiUsGNAB7%2F4FJmr8A10uJpCb5NjkEjKTRiCx1s%2BCFbVibGZNM0isuYy41nMTaytX%2BghWfr3KyBbAe1slVAOuTS9Jzr2NdhTHW0dw6kp14sSz0GBX4%2Fi4t7VKCjDNTiOXC9fR6MiShy%2FPTXHGxqx2z5yrahytccGIU4Pp8irmm3kTJ%2FnBaOcrj0kFzzcArTxbncGcT1cjP0KVrhlOPvQP2EIeqWQeQP6HGarx10who2%2BY59HWNzGZlc4mHpTIPaIyMRqn5yxUnodhy45mUR9cAVqEOw17AumuwYriCS%2FRc0t1arCJN%2B8kMcF8zxXKJEfCK4yBcDKLEdYzHpXWd2C1I6%2BBOx6mx1hmucOoGDSvsrhVUkVHSCN3i6cVl5dhbCMrdbKKnze1YcM0sJ21dsF9JU8%2FYswDfbjC%2B3XfQW%2Ffnzs%2Fmd%2FaAqmQG8Ua2Ld%2FZ2AV7Q9lSlzk4dcPc2iaK5mcKfGzh4Fth%2BfCfr3r65JWSv7o1%2BHuXTBFm9tGJ7%2FASCnEkKnWhy%2FwNM8W10Bwc%2Bdz0yq%2BnvCBc4OVc1E4%2Bs3XrL7zzrYvv0InFjNRu1zfloOuMVOzlq%2FwJi2CylLKDXKE3kLAFDXcXjBZ8Ip1eYG4maOHM5swVPQenfob81poInfuyi%2F0B8tVGXshyvH6baUmcj3Fuw2N0SX4l9s5nCF%2FLIpLDYwPtRh0PM86NKY%2Bv7pSzrdTed3wpq0BxLpNRrWlvvxlxxG4c%2FcfKDgUJ2yY7voz9Rd6uB1Ntlz7mSs7MH23GW6v5OzxnwLai88vNsF60H8lJDeihv%2Fg9fwi8aQEc6dyKqlHoarOMLjbCs%2BX80m%2F221hN0IiyiTsk%2BScn4MH%2Be5M%2B%2FOP5f47%2FABRC7md%2F2UDNAAAAAElFTkSuQmCC)](https://github.com/Dani3lSun/apex-github-badges)
[![APEX 20.1](https://img.shields.io/badge/APEX-20.1-blue.svg?style=flat&logo=data%3Aimage%2Fpng%3Bbase64%2CiVBORw0KGgoAAAANSUhEUgAAADwAAAA7CAQAAACN8CFBAAAHHUlEQVRYw%2B1ZaUxUVxQGq4g1qNVqW0M0qXWLiqmWRHDp2KCZH9CqUWPEbVqxVJS21lQndYmaGiBAAXEBEcEAMVSUsAwwzIADwyo7CAgIqKyyzsIMs96q%2BN65784bGZB%2F9f5795xzv3vPOfcs91lZfRhvxrbVKU4ZTt5r3m%2BVA4uvOd1yOu%2B0dZZF7KfnPyvTodfDgGStSV%2BPBzJ4VnbWYO%2FIKgjJUefT2ydHEQlfM5iJsNHbI3QaK2yAU3MtIoYG1d0%2BOcOsSNTy9mpSpL83Y9WYTrvqaS9iHY9C19myity1HXrGJqBSCudZChs0r0sJkgakRUZspZC9LCIxnw11A0tjS246fKlVQgdLYH0delQg9aIpYWvi0uAAUEBepYlI4lfGBhB53By2INq2%2FqqBnhnoF24aDdZ%2F0%2FN%2BWKOo6doXI%2FOitT3UVhBnGiFUmQQiTS3hc1%2FPxU9ujtaDrftEzu%2BCDXRu7aN4jaimLtQOaFIxNe9hzxBymwVbbWnAKS1RAK2QixaZte2iDjkGW8Okiu5QNG8m8Hl7OG3EFJwSb%2F3kCuhCr09dxgZ7eZkc9ocKGoMnM%2BlVYormyQTm0cBqFBXNFLo%2FtcEPPFMpT%2BeYwHK65AArqQ%2F6lLikocPUsZALsSWrato%2BQyjyFseGAT2lMRQONNifsYUBu6WtH5ScXxfwCXPl0oNa2tML0kyUJd6jBoWi6BAOcdVbwwC6owfmfRw7ZQBbXkauW7fbSF8NOfJ1YbFTAg8zE4q%2F4fIRk%2F40dEThOn3oKWru6gqZFmTyq8k1H7tj%2FoFEPFa%2F5E%2BK2jNMs2mR6C6TfsI25d5ryr%2BedEz%2Bth8EkLA20I4pUeGl00KsFu8Jm2T2Lgo9lVhYF8W7MDw8ySY5Ic2d%2BvJz7cCUnFlL2rbiuFYNLvvIc5To89BrCFOO8BZ3GjufzxbctkXFAcRpangGHcCWelkQb1N4mP5QZgR3qilPiOOAGmALi01ciocwo0l5FmYYf1cNgmXFCSaw61VYyhHUkKet8IaUpEX3XC3OqHzrB%2B5KbMeSFFds6ZBtPUOwreSqQCK9V5zSaSAm5LuHWY%2BpihAfVtDQMk38dDomb%2B%2BUQ7YVFfoQhqj01msBtuzwOOqm9IMjB1OqIo%2FSsJxeFcBKckiZek8sh6PCg%2BOsEm%2B6DRu0unB619c5w5jtU4pI%2FupfsRrLkOQ27vKUbx3oFkCnhMDtMg3AxpZfJC5axTm4QCqU7BZrbTURI2jvSyUoObHwwscE7BmIUkpU5D5BBX4w5sl6lCUm6U9%2BNxoBtmTfBMFGcIcMcNr0LJJe%2Bwdca7VB9MMEwV7ehkeyqFKSXnQJg0VhGyYI1ocHwdGAIovPEi5V7KvXgZLFE3Va3wN9mG2TMkwu0FkDbQQFKtxNx%2FvFcQfeAzZsh0ILsAKBiUvxQclDKI8%2Bbf6S7jadVrJjnLA3duLhIjabpFdhtlVpY%2Bmau3hOf%2BfIbPbO8dj2sFIHsAGFfBsmvTAElKxEqd%2FRSp42%2BJKa1%2BlSxxqr%2Fz46oAIl30k%2FSdRfJX4GPdhW%2Bj1WpVgnBGiwnktwdAywiUsGNAB7%2F4FJmr8A10uJpCb5NjkEjKTRiCx1s%2BCFbVibGZNM0isuYy41nMTaytX%2BghWfr3KyBbAe1slVAOuTS9Jzr2NdhTHW0dw6kp14sSz0GBX4%2Fi4t7VKCjDNTiOXC9fR6MiShy%2FPTXHGxqx2z5yrahytccGIU4Pp8irmm3kTJ%2FnBaOcrj0kFzzcArTxbncGcT1cjP0KVrhlOPvQP2EIeqWQeQP6HGarx10who2%2BY59HWNzGZlc4mHpTIPaIyMRqn5yxUnodhy45mUR9cAVqEOw17AumuwYriCS%2FRc0t1arCJN%2B8kMcF8zxXKJEfCK4yBcDKLEdYzHpXWd2C1I6%2BBOx6mx1hmucOoGDSvsrhVUkVHSCN3i6cVl5dhbCMrdbKKnze1YcM0sJ21dsF9JU8%2FYswDfbjC%2B3XfQW%2Ffnzs%2Fmd%2FaAqmQG8Ua2Ld%2FZ2AV7Q9lSlzk4dcPc2iaK5mcKfGzh4Fth%2BfCfr3r65JWSv7o1%2BHuXTBFm9tGJ7%2FASCnEkKnWhy%2FwNM8W10Bwc%2Bdz0yq%2BnvCBc4OVc1E4%2Bs3XrL7zzrYvv0InFjNRu1zfloOuMVOzlq%2FwJi2CylLKDXKE3kLAFDXcXjBZ8Ip1eYG4maOHM5swVPQenfob81poInfuyi%2F0B8tVGXshyvH6baUmcj3Fuw2N0SX4l9s5nCF%2FLIpLDYwPtRh0PM86NKY%2Bv7pSzrdTed3wpq0BxLpNRrWlvvxlxxG4c%2FcfKDgUJ2yY7voz9Rd6uB1Ntlz7mSs7MH23GW6v5OzxnwLai88vNsF60H8lJDeihv%2Fg9fwi8aQEc6dyKqlHoarOMLjbCs%2BX80m%2F221hN0IiyiTsk%2BScn4MH%2Be5M%2B%2FOP5f47%2FABRC7md%2F2UDNAAAAAElFTkSuQmCC)](https://github.com/Dani3lSun/apex-github-badges)

Deploy a complete Oracle APEX Development stack on Docker using Docker Compose. This stack is base on the Oracle Database, and Oracle REST Data Services (ORDS) image builds defined in this repository.

The following article provides a description of this stack definition -> [Docker : Oracle APEX Stack - Docker Compose](https://reybis.com/posts/oracle-apex-stack-docker)

- [Oracle APEX Stack on Docker](#oracle-rest-data-services-(ORDS)-20-on-docker)
	- [Preview](#preview)
  - [Software](#software)
	- [Directory structure](#directory-structure)
	- [How to use](#how-to-use)
			- [Run the stack](#run-the-stack)
	- [Credits](#credits)
  - [Changelog](#changelog)

## Preview
![](https://github.com/reybis/oracle-apex-docker-stack/blob/master/preview.gif)

## Software 
Due to licensing restrictions I can't host these files in Github or elsewhere. 

As such, you'll need to download them manually. Download the following files and store them in the respective `software` folder.
- [apex_20.1.zip](http://www.oracle.com/technetwork/developer-tools/apex/downloads/index.html)
- [LINUX.X64_193000_db_home.zip](https://www.oracle.com/technetwork/database/enterprise-edition/downloads/index.html)
- [apache-tomcat-9.0.37.tar.gz](https://tomcat.apache.org/download-90.cgi)
- [OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz](https://adoptopenjdk.net/releases.html?variant=openjdk11&jvmVariant=hotspot)
- [ords-20.2.0.178.1804.zip](http://www.oracle.com/technetwork/developer-tools/rest-data-services/downloads/index.html)
- [sqlcl-20.2.0.174.1557.zip](http://www.oracle.com/technetwork/developer-tools/sqlcl/downloads/index.html)

## Directory structure
Directory contents when software is included.

```
.
ords/ol7_ords
  ├── Dockerfile
  ├── README.md
  ├── scripts
  │   ├── healthcheck.sh
  │   ├── install_os_packages.sh
  │   ├── ords_software_installation.sh
  │   ├── server.xml
  │   └── start.sh
  └── software
      ├── apache-tomcat-9.0.37.tar.gz
      ├── apex_20.1.zip
      ├── OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz
      ├── ords-20.2.0.178.1804.zip
      ├── put_software_here.txt
      └── sqlcl-20.2.0.174.1557.zip
database/ol7_19
  ├── Dockerfile
  ├── README.md
  ├── scripts
  │   ├── healthcheck.sh
  │   └── start.sh
  └── software
      ├── apex_20.1.zip
      ├── LINUX.X64_193000_db_home.zip
      └── put_software_here.txt
```

<!-- lb/nginx_lb
  ├── Dockerfile
  ├── README.md
  ├── scripts
  │   ├── healthcheck.sh
  │   └── start.sh
  └── certs
      └── put_certs_here.txt -->

## How To use 

### Run the stack
```
docker-compose up
```

## Credits
Oracle-base docker files by [Tim Hall](https://github.com/oraclebase/dockerfiles)

## Changelog

#### 1.0.0 - Initial Release