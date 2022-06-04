## Conti RaaS group chat leaked (English translation) about firmware exploit and implant

A leaked XMPP internal chat from Conti group revealed by [vx-underground](https://share.vx-underground.org/Conti/). The developer of Conti group mentioned about how they leveraged the CSME for further SMM implant:


Oct 29 2020
-------
"according to ideas, if regarding the topic that I’m doing, since I’m changing the flash drive, there is an idea to make not just a file dropper, and running them under the OS, but an SMM driver for remote data collection, memory dumps, etc."
"maybe you just heard about ME, there are working POCs for SMM"
"in fact, I am finishing a module that can put anything into the firmware, as long as it is a driver with a file system and file drop, then you can develop an SMM driver and put it into the firmware"

Jun 7 2021
-------
"Hello, you’re doing well. I apologize for not answering right away, I haven’t communicated through a toad for a long time, I didn’t see what you wrote. Now I am finishing a full report on the mechanism of operation of the Intel ME controller and the AMT technology based on it. Restored a bunch of undocumented commands with the help of reverse, interaction interface dump and fuzzing. Unfortunately, the starting theory based on the presentation of the Embedi/PositiveTechnologies researchers was not confirmed in the form in which they presented it, but there is another legal mechanism to activate AMT, but so far it has not reached a working PoC, at the moment I am making a buffer sniffer that provides the HECI interface, because this is all configured in UEFI, then the sniffer took a little longer, after I completely restore the command set, the PoC will be prepared. There are ideas, if we talk about uefi, then this is not just a load dropper, but also possibly some kind of daemon of the SMM level of handlers, plus. Now I have closely studied the ME controller, then there are ideas to test such functionality as rewriting an SPI flash drive through it. Usually this controller is allowed to write to a flash drive, which cannot be said about the processor, and some commands have been discovered that are responsible for this functionality."

Unfortunately, the starting theory based on the presentation of Embedi/PositiveTechnologies reporters was not confirmed in the form in which they presented it, but there is another legal mechanism to activate AMT, but so far it has not reached the working SOFTWARE, at the moment I make a sniffer buffer that provides the HECI interface, because it is all configured in UEFI, then the sniffer took a little longer,  after I fully restore the command set, the POC will be prepared.
