![](https://uwe-cyber.github.io/images/uwe_banner.png)

# Activity: Cyber Funfair

## Activity Overview

This activity requires the setup of some LEGO rides which are controlled  by a Raspberry Pi acting as a Cyber Physical Systems (CPS) server. The CPS can be attacked to show case the impact cyber attacks can have on physical systems, as well as providing learning opportunity for Network Traffic Analysis (NTA) using [Wireshark](https://www.wireshark.org/faq.html#_general_questions). 

Depending on the attack the LEGO rides will stop, slow down or speed up, these physically observable changes should help point students to the fact an attack is underway and can be used in conjunction with NTA and the provided Graphical User Interface (GUI) to identify and counter the attacks.

## Session Duration

45 minutes

## Curriculum Links and Key Concepts

* [Fundamentals of computer networks ](https://www.bbc.co.uk/bitesize/guides/z777xfr/revision/1)
* [Fundamentals of cyber security](https://www.bbc.co.uk/bitesize/guides/znnny4j/revision/1)
* [Network topologies, protocols and layers](https://www.bbc.co.uk/bitesize/guides/z666pbk/revision/1)
* [Network Traffic Analysis (NTA)]
* Cyber Physical Systems (CPS)

## Activity Setup

The following components support 2 groups of 5 -6 students:
* 1 x LEGO Spike Kit (Prime Set)
  * 2 x LEGO rides using 1 motor each
  * 1 x LED colour matrix
* 1 x CPS server (Raspberry Pi with Pi Build Hat)
* 1 x Attack Machine (Pi 400 + screen) 
* 2 x Student laptops (running Kali Linux)
  * With the CPS and GUI code downloaded
* 1 x Wireless Access Point (WAP, Raspberry Pi 3b or later)

## Activity Exercises

There are 3x attacks that can be run:

* Denial of Service (DoS)
* Code Injection
* Man in the Middle (MitM) – This also impacts the LED colour matrix

Each attack will have it’s own impact on the LEGO ride under attack and will produce different network traffic.

The provided GUI has sections for the different attacks, the expected impact on the rides and what students should see in the network traffic. A separate countermeasures page allows students to counter the attack, allowing the ride to run normally while the attack is still ongoing, so they can see successful implementation of their countermeasure.

Students are able to work through the exercise independently using their observations, NTA and the GUI or can be assisted by a teacher if required.

## Activity Learning Outcomes

* An understanding of what a CPS is and the impact of cyber attacks
* An understanding of NTA and how it can be utilised

Further resources linked to the Cyber Body Of Knowledge (CyBOK) are also included and students are encouraged to explore these.

## Further resources 

* [Supporting documentation](https://uwe-cyber.github.io/lego_funfair/cybok_report.pdf) (In depth setup and session support)
* [ISO images](https://uweacuk-my.sharepoint.com/:f:/g/personal/alan_mills_uwe_ac_uk/EguGmVOVJOhAj-4CQQWQ0n0BnZEgcUpmoO27nFCRBLGjdQ?e=z9Lvkb) (for the CPS, WAP and Attack Machine)
* [GitHub – Code Repository](https://github.com/uwe-cyber/Future_Funfair) (CPS and GUI code)

Building instructions – For all instructions plug rides directly into the CPS
* [Ferris Wheel](https://assets.education.lego.com/v3/assets/blt293eea581807678a/blt0d2abaf129110763/5f572fa927a6ca5b5b1a6e45/U2L6.pdf?locale=en-us)
* [Seated swing](https://assets.education.lego.com/v3/assets/blt293eea581807678a/bltff64b9fa4934e499/5f572f9cead1c447eca8fdd1/U2L3.pdf?locale=en-us)
* [Teacups](https://assets.education.lego.com/v3/assets/blt293eea581807678a/blt27cf3aba3ebccf38/5f572f6c4b239959f43aa72a/U2L2.pdf?locale=en-us)


