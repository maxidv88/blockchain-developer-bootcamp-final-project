# Idea 1 - File Integrity Monitor

## The Problem

Organizations depend on their software and data to function. Often times, if files related to these software get corrupted, or are maliciously tampered with, it may cause massive problems for the organization. Problems can range from their services being unavailable (Denial of Service) to execution of malicious code in their environment. Thus, ensuring the integrity of important files in the organization is of significant importance.

File Integrity Monitoring (FIM) is a process that organizations can use to test and ensure that files such as Operating System files, Database files, and application files have not been corrupted or tampered with. With FIM, a baseline can be established that allows an organization to verify whether an file has changed (been corrupted or tampered with). This is done by hashing the file and storing the hash in a secure database. The organization can then check the hashes of files at a given interval against the baseline of hashes stored in the FIM database to verify whether the files have changed or not.

However, the FIM database itself must be secured such that it is not corrupted or a malicious actor cannot alter its contents. For example, if a hacker wants to swap a critical software dependency for an application in the organization's environment with their own malicious one, and they are able to change the value of the hash of this dependency file in the FIM database, it would defeat the purpose of using a FIM solution.

## Purpose

Blockchains are a great database solution when data integrity and immutability is of utmost importance. A blockchain-based File Integrity Monitoring solution would solve the problem of malicious actors tampering with the database to hide their actions relating to file changes.

The Blockchain FIM solution would ensure that once a baseline has been created, it cannot be altered. Furthermore, the blockchain solution would also allow the organization to verify who created the baseline and who updated any records because each transaction would be signed with the private key of the user.

## User Flow

1. User interacts with a smart contract to create a baseline by providing files that they want to monitor for changes
2. Smart contract is provided with the files' properties and their respective hashes, which are written to the blockchain
3. A FIM client runs in the user's environment, monitoring the files by checking against the data stored on the blockchain to ensure the monitored files are not tampered with


## To Consider

* It is quite normal to update certain files. For this reason, the user must be able to update the hash of a file in the baseline. In order to do this, a user can use their private key to send another transaction to the smart contract to update the file in question with the new hash. The old hash would still be on the blockchain but it will be superceded with the new hash. This also allows one to audit changes made to files through time.


# Idea 2 - Social Media NFT

## The Idea

The user can log into a website using the "Log in with Twitter" or "Log in with Facebook" button. This verifies that the user indeed has access to the given social media profile. Once logged in, the user can mint an NFT that represents their social media account. This NFT would represent ownership of their social media account. Only one NFT can exist for any given account.


## Purpose

The purpose of this project is to allow owners of social media accounts to prove their ownership using NFTs. Additionally, if a user wanted to transfer the ownership to a different user, they could transfer the related NFT to that user as well. This would allow one to look at the history of the social media account ownership. Or in the case of an account hijack, the NFT would still be owned by the original user and the user could prove that they own the account, not whoever hijacked it.
