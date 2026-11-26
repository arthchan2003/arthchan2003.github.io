---
title: "Issue 53 - GTC 2018"
date: 2019-07-17
---

# Issue 53 - GTC 2018

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 53 *March 31st 2018* ](http://aidl.io/issues/53/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

GTC 2018 was happening last week. So we have a special session with five items. Check out our notes on DGX-2, and Nvidia/ARM deal.

---

As always, if you like our newsletter, feel free to forward it to your friends/colleagues!

This newsletter is a labor of love from us. All publishing costs and operating expenses are paid out of our pockets. If you like what we do, you can help defray our costs by sending a donation via [link](http://paypal.me/aidlio/9). For crypto enthusiasts, you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Artificial Intelligence and Deep Learning Weekly

## GTC 2018

### [GTC 2018 Keynote](https://www.youtube.com/watch?v=95nphvtVf34)

Summary: 
- New Quadro with 32G HPM,
- V100 now also has 32G HPM. PCGames was [disappointed](https://www.pcgamesn.com/nvidia-volta-gtc-catchup) because there is no GeForce [GTX11XX series upgrade], (https://www.digitaltrends.com/computing/nvidia-geforce-gtx-11-series-not-20-series/) as rumored
- DGX-2,
- The NVSwitch switching architecture within DGX-2,
- The Issac SDK, a robotic toolkit built on top of Jetson,
- Kubernete container with CUDA acceleration.

Wow, quite a keynote. Many of these new products will have impact on deep learning.

[youtube.com](https://www.youtube.com/watch?v=95nphvtVf34)

---

### [Nvidia's Own Report](https://blogs.nvidia.com/blog/2018/03/27/nvidia-gtc-2018-gv100-dgx2-hyperscale-datacenters/?ncid=em-ded-ndcgnr-35399&mkt_tok=eyJpIjoiTmpGbFpEY3dPVFl4TmpneCIsInQiOiJQN2tqT2U3VW5BOVl0YThrS1ZWK3RNOU93NFZuMzg5VDdncEdxbGpuTEo3VEcyaHFTMlJydDFRT2ZjZlp3UGdsU0hmVSs1VEw4NW9EcnU3SUxFWkJIUEtIcVJOakFjWlZFaGc0VnU3WFBmckJmbklBOW94YzRkQzc5ZmRpWWVyZiJ9)

A good summary of what's going on at GTC 2018.

[nvidia.com](https://blogs.nvidia.com/blog/2018/03/27/nvidia-gtc-2018-gv100-dgx2-hyperscale-datacenters/?ncid=em-ded-ndcgnr-35399&mkt_tok=eyJpIjoiTmpGbFpEY3dPVFl4TmpneCIsInQiOiJQN2tqT2U3VW5BOVl0YThrS1ZWK3RNOU93NFZuMzg5VDdncEdxbGpuTEo3VEcyaHFTMlJydDFRT2ZjZlp3UGdsU0hmVSs1VEw4NW9EcnU3SUxFWkJIUEtIcVJOakFjWlZFaGc0VnU3WFBmckJmbklBOW94YzRkQzc5ZmRpWWVyZiJ9)

---

### [DGX-2](https://www.nvidia.com/en-us/data-center/dgx-2/)

"Monstrous" and "beastly", these are the adjectives which outlets use to describe the new DGX-2. Indeed, upgraded from DGX-1, DGX-2 now pack 16 Volta V100s into one single machine.

Perhaps worth a mention is the NVSwitch architecture. You can imagine building a DGX-2 is not just about putting 16 cards in a single machine. To truly utilize 16 Voltas, you also need to think of increase the throughput of transferring data to/from the GPU cards. [NVSwitch](https://www.nvidia.com/en-us/data-center/nvlink/) seems to be the answer.

(Note: We also learned that AIRI and GTX-2 are different products with similar price tag. AIRI was created by a partner of Nvidia, Pure Storage, and it costs $600k. Whereas DGX-2 is Nvidia's own, and it cost $400k. Also see "Deals".)

[nvidia.com](https://www.nvidia.com/en-us/data-center/dgx-2/)

---

### [AutoSIM and Drive Constellation](https://techcrunch.com/2018/03/27/nvidia-debuts-new-drive-constellation-simulated-self-driving-test-system/)

Nvidia designed a new simulation system which help partners to develop real-driving experience. This is likely a big boost for vendor tries to build their own SDC.

[techcrunch.com](https://techcrunch.com/2018/03/27/nvidia-debuts-new-drive-constellation-simulated-self-driving-test-system/)

---

### [Nvidia and ARM](https://www.forbes.com/sites/marcochiappetta/2018/03/27/nvidia-and-arm-partnership-to-bring-deep-learning-technology-to-iot-devices/#7095f4217520)

This is a quiet launch and it doesn't receive much attention as GTC 2018 - Nvidia is partnering with ARM to port [NVDLA](http://nvdla.org/primer.html) to IoT devices. NVDLA was first designed for the DriveDX platform as an SoC. The partnership deal is to integrate NVDLA into [Arm Project Trillium](https://www.arm.com/news/2018/02/arm-project-trillium-offers-the-industrys-most-scalable-versatile-ml-compute-platform), which include the Arm machine learning (ML) processor and Arm object detection (OD) processor.

[forbes.com](https://www.forbes.com/sites/marcochiappetta/2018/03/27/nvidia-and-arm-partnership-to-bring-deep-learning-technology-to-iot-devices/#7095f4217520)

## News

### Partnership

- [Apple, IBM extend Watson-CoreML Coupling](https://techcrunch.com/2018/03/19/apple-ibm-extend-partnership-with-watson-core-ml-coupling/)
- [AIRI, collaborated by Pure Storage and Nvidia](http://www.theregister.co.uk/2018/03/27/pure_nvidia_ai_airi/) - Connecting four DGX-1, while not exactly DGX-2, it prices similarly (at ~600k) and is a monster of itself.

Artificial Intelligence and Deep Learning Weekly

---

### Deals

- [Digital Reasoning $30M](https://www.wsj.com/articles/ai-company-digital-reasoning-raises-30-million-led-by-bnp-paribas-1521510263)
- [Mythic $40M](https://www.xconomy.com/san-francisco/2018/03/20/ai-chip-startup-mythic-reaps-40m-from-softbank-lockheed-venture-arms/)
- [17ZouYe $250M](https://e27.co/temasek-leads-us250m-series-e-round-chinese-ai-edtech-firm-17zuoye-20180321/)
- [Intercom Series D $150M](https://www.cnbc.com/2018/03/26/intercoms-new-funding-brings-valuation-to-1-point-275-billion.html) - first project is allegedly an AI project.

Artificial Intelligence and Deep Learning Weekly

---

### [Google released TTS API based on DeepMind's Wavenet](https://www.theverge.com/2018/3/27/17167200/google-ai-speech-tts-cloud-deepmind-wavenet)

We learned about this for a while. But Google is now officially using DeepMind's Wavenet technology for its text-to-speech API. Also see Google's original [post](https://research.googleblog.com/2018/03/expressive-speech-synthesis-with.html).

[theverge.com](https://www.theverge.com/2018/3/27/17167200/google-ai-speech-tts-cloud-deepmind-wavenet)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 120,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly
