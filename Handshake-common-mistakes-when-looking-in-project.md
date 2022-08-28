# Handshake: Common mistakes when looking into the project.
Hey namers! Today I've been sitting in Handshake DNS discord, and accidently looked into #shitpost channel. Then found [this article](https://akshat.sh/posts/handshake-scam/).

I've read it, and obviously I understood that person didn't dig enough and didn't ask question "why?". Then I thought and understood that everybody can make such mistakes when looking in handshake.

So I decided to answer to author of this post and everybody else who will have same questions.

So let's start.

## Conflicts problem
![image](https://user-images.githubusercontent.com/40735471/187086332-ba1c0e76-cf6c-4135-808a-aecd5b7bdaff.png)
So, as author stated, handshake not intends to respect other naming systems' new TLD appears.

Why? Answer is very easy. Handshake won't sacrafice its souverignity and decentralization just to achieve minimal name colision.

Handshake intend to fight monopolized name systems, not integrate with them.

Imagine there's handshake TLD: .abc

This TLD is staked on some dSLD service, and already brings big income to person who registred it. And then, after some time, some registrar submits application to ICANN, and asks to register his own .abc. Will ICANN respect hadshake network and refuse application just to avoid colision? I doubt that.

So what should Handshake do in this situation? Do hardfork, remove rights from .abc owner because "Uh oh, another registrar registred this name, so we should pass them control, they're more main than us"?

The right answer is obviously not do anything and stay with name colision. Who judges which registrar should be "main"? So lets just leave control to ourselves.

Otherwise we just put handshake in the bottom of list of name systems by power of TLD ownership, which creates depend on other name systems and centralizes project.

Name colision can be only avoided when name service TLDs registration is controlled by centralized entity (ICANN, ENS DAO, etc.). Then project owners can make sure that there's no colisions before registring its name, and register without competition with other namesystems.

In decentralized TLD registry systems (Like handshake) you can't accept such behavoir. 

The best way to avoid colisions for TLD owners on other naming systems will be just respect handshake and register domain as specified in its protocol (via auction or buy from current owner).

If new TLD owner not respects Handshake's protocol of registering names, why should Handshake's protocol of registering names respect new TLD that appeared on different registry?

## PoW blockchain
![image](https://user-images.githubusercontent.com/40735471/187087567-c7cf87b2-5411-4f39-ae26-4de3faea4a1d.png)
It comes to long discussion of which proof algorithm is best. This discussion have been in crypto-related resources for long years, and PoW still is one of the best.

However, in handshake reason why it should be PoW is simplier than it seems, we just have to open [handshake's whitepaper](https://handshake.org/files/handshake.txt).

Now search for "proof of work", and you will find reason why PoW fits handshake the most.

![image](https://user-images.githubusercontent.com/40735471/187087718-276c70ee-649d-4099-aa21-b40ea6150cc7.png)

Proof of work allows handshake to have trusless lite nodes (if you know Proof-of-Stake RPC centralization hell, you will be already excited).

The thing is that only Proof of Work allows to have resilience against fraudulent SPV proofs.

Saying with simple words, if you try to run lite node on PoS, you will have chance to get wrong info about chain.

Proof of work allowed handshake to have lite resolvers of handshake-based names. See [hnsd](https://github.com/handshake-org/hnsd) and [fingertip](https://impervious.com/fingertip).

These resolvers allow seamless resolving of handshake-based domains with just 10-20mb RAM in usage and 0% CPU/GPU usage. (In opposite, ethereum is not having support of SPV nodes, and to achieve permissioless resolving of ENS/Unstoppable Domains you will have to run full ethereum node on your PC, which requires terabytes of disk space and strong CPU/GPU. and this all only to resolve domain. Otherwise you're most likely trusting gateway or RPC node (In most cases Infura's) )

## You cannot actually use your domain
![image](https://user-images.githubusercontent.com/40735471/187088175-3b070161-f802-454d-ac4c-e94e712f91b1.png)
And there comes not understanding purpose of decentralization. In short, if these DNS providers provided support for handshake names, handshake would be useless or just became second ICANN.

Handshake is *decentralized* TLD system. What is sense of its decentralization if we anyways rely on *centralized* DNS providers?

It is like to ask these DNS providers to integrate .onion natively. They of course can do it, and even host gateway for you, but what's the sense then?

Sense of Tor is anonymous access to network, while if we anyways pass all the data to our DNS providers, tor becomes useless for us.

So .onion integration with DNS providers is absolutely useless: Sense is lost.

Same with Handshake domains. If we just rely on centralized DNS providers, sense of TLD decentralization is fully lost.

However, due to PoW nature, we can install lite SPV client and everything will stay seamless (it will just serve you somewhere in background, not interrupting you).

## It acts like Ponzi scheme
![image](https://user-images.githubusercontent.com/40735471/187088480-2e9c021f-195f-427b-abcd-a9b9c5aafcfb.png)
For start, let's remember ENS (Maybe UD too, but not very sure about it), where 90% of bought domains appears on OpenSea after some short time.

Let's now move 20 years before, where only ICANN DNS existed.

There's unregistred good domain, a.com for example. You know it and realize its potential.

I don't know what would exactly you do, maybe just leave it because "Maybe some dev will come and use it later... Will leave it for him!", but I would just buy this name (I am not dumbie and I understand value of it, I will resell it later).

Also remember early .com years. There were literally race about who will register more good .com names. Same with handshake now. Anyone can use handshake for anything, be it hosting site, reselling with higher price or selling SLDs.

Thinking that only devs and people who will use domain are allowed to register HNS name is naive. 

## End notes
![image](https://user-images.githubusercontent.com/40735471/187088865-b397fd4f-09db-4bc5-a5b1-76b65eb4cf3f.png)

And there finally I found sentence with which I can agree! "Buying HNS domains on a centralized registrar, with no ability to transfer your domain, defeats HNS’s purpose".

It is very true, and Namecheap perfectly understands that, that's why they're actively working on decentralized SLD (dSLD) development. 

Here's document about how are they planning to make it live: https://github.com/namebasehq/decentralized-slds

Also there's already live example of dSLDs, Impervious Registry: https://impervious.domains/

Wish better dig in projects when discovering it, lovely, your mouse/.
