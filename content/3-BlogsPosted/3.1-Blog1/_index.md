---
title: "Blog 1"
date: 2026-07-08
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---


# Why Epic Games Developed Lore and How AWS Helps Optimize Binary Assets Storage

Hello AWS Study Group VN community. I would like to share this post with you.

If you have ever developed a game with thousands of textures, models, animations, or engine binaries, you have likely noticed that traditional version control systems like Git are not well-suited for binary files. Every time you edit a file of a few hundred megabytes, the system usually has to save almost the entire file as a new version, even if only a tiny fraction changed. Over time, the volume of data grows extremely fast, leading to ever-higher storage costs.

To solve this challenge, Epic Games developed **Lore** – an open-source version control system designed specifically for binary assets. At the same time, AWS introduced a reference architecture to deploy Lore on the cloud.

In this blog post, we will explore:
* How is Lore different from traditional version control?
* What does the deployment architecture on AWS consist of?
* Why does this model help optimize storage costs?

---

## 1. How is Lore different?

Instead of saving the entire file after each modification, Lore splits each binary into multiple fragments (chunks) and identifies them using cryptographic hashes. This means:
* Only fragments containing changed data are stored.
* Existing fragments are reused.
* A fragment that appears in multiple files or multiple projects is saved only once.

As a result, the rate of storage capacity growth decreases significantly as the project develops.

---

## 2. Why does Lore save costs?

AWS highlights three prominent benefits:
* **Reduced storage capacity**: Only stores the changed data fragments instead of the entire file.
* **Almost free branching**: New branches only reference existing fragments, creating no extra data if the assets are unchanged.
* **Cross-project data sharing**: Duplicate fragments are saved only once, optimizing resources at the studio scale.

---

## 3. Lore Architecture on AWS

AWS implements Lore with several familiar services, each playing a distinct role to ensure performance and scalability:

* **Amazon EC2 (Edge Pods)**: Receives connections from clients and caches fragments on NVMe drives to accelerate access.
* **Amazon ECS (Write Tier)**: Handles deduplication (eliminating duplicate data) and writes new data.
* **Amazon S3**: Securely stores unique fragments for the long term.
* **Amazon DynamoDB**: Manages metadata, locks, and branch information with millisecond latency.
* **AWS Cloud Map**: Helps Edge Pods automatically discover the Write Tier via internal DNS.

This architecture allows the system to scale easily while reducing load on the primary storage layer.

---

## 4. When to use Lore?

The Lore system is particularly suited for:
* Game studios with many collaborating artists and developers.
* Projects containing a large volume of binary assets.
* Businesses developing multiple game titles at the same time.
* Teams wishing to optimize storage costs and synchronize data quickly on AWS.

---

## Conclusion

Lore brings a new approach to managing binary assets by dividing data into reusable fragments, rather than saving the entire file after each edit.

Combined with **Amazon EC2, Amazon ECS, Amazon S3, Amazon DynamoDB**, and **AWS Cloud Map**, this architecture helps:
1. Reduce storage costs significantly.
2. Speed up the asset synchronization process.
3. Support efficient branching.
4. Leverage cross-project data reuse.
5. Scale easily as the studio grows.

For game studios working with large volumes of binary assets, this is a highly recommended approach to building a modern version control system on AWS.

> **Original Article:** [How Lore rethinks binary asset storage on AWS](https://aws.amazon.com/blogs/gametech/how-lore-rethinks-binary-asset-storage-on-aws/)  
> **Tags:** #AWS #AWSForGames #EpicGames #Lore #AmazonS3 #AmazonDynamoDB #AmazonEC2 #AmazonECS #CloudArchitecture #GameDevelopment #VersionControl #BinaryAssets #StorageOptimization
