[return](gnuhealth)

:verifyprivatekey:

```sh

#gpg opensource software is basically very simple
#first download the public key of the software creator, then download the private key which is called the detached signature of the software version _and finally simply make that public key verify the private key of that latest software version

#gpg signing is using asymetrical keys that is also they same 
#with asymetrical encryption but its reverse.
#in gpg signing and verifying, the private key of the program
#developer signs and the public key veryfies the private key signature
#download the public key
#guge
gpg --recv-key  --keyserver  keyserver.ubuntu.com 0xC015E1AE00989199

#The key is issued by Luis Falcon (meanmicio at GNU) <falcon@gnu.org> and its fingerprint 
#is ACBF C80F C891 631C 68AA 8DC8 C015 E1AE 0098 9199. This information can be seen issuing:

#guge
gpg --with-fingerprint --list-keys 0xC015E1AE00989199

#Then, verify the signature, using the matching version number for the latest. 
#For instance, if latest GNU Health version is 4.0.4, then
#Download the detached signature:
#guge
wget https://ftp.gnu.org/gnu/health/gnuhealth-4.0.4.tar.gz.sig

#Verify the package using the detached signature with the public key
#guge
gpg --verify gnuhealth-4.0.4.tar.gz.sig gnuhealth-latest.tar.gz

#The important part is the Good signature from "Luis Falcon ....". The WARNING means that, 
#even if the file and signature are OK and validated correctly, you aren't trusting that key; 
#and it's OK. You can read more about this in The GNU Privacy Handbook, Chapter 3. Key Management.
#If the file is correctly validated, the output should be something like:
gpg: Signature made Sat 01 Jul 2017 11:06:25 PM WEST
gpg:                using RSA key ACBFC80FC891631C68AA8DC8C015E1AE00989199
gpg: Good signature from "Luis Falcon (GNU) <falcon@gnu.org>" [ultimate]
gpg:                 aka "Luis Falcon (GNU Health) <lfalcon@gnusolidario.org>" [ultimate]

```






