# SocialNetworkLaw
Security and Dependability of Distributed System

To initialize the community, one of the founders should send requests to other members about their thought of community formation. Message format: {"type": "beginCommunity"}

Other founders should approve formation of this community. Message format: {"type": "communityBeginApproval", "approval": "yes"}

The community is formed when all the 3 founders approve the creation of this community.

The Directory Service for out community is named "manager"

Users should now send requests to the manager to become a part of this community. Message format: {"type": "register", "name": "user1"}

Each user becomes a member only when their request has been approved by all the founders. Each founder should send their approval to that particular user. Message format: {"type": "userApproval", "approval": "yes"}. This message should be sent to the user directly.

To remove a particular user, any one of the founders initiate this process. Message format: {"type": "revokeUser", "name": "user1"}

manager@192.168.1.10 {"type": "createGroup", "groupName": "group1"}

manager@192.168.1.10 {"type": "deleteGroup", "groupName": "group1"}

manager@192.168.1.10 {"type": "getAllGroups"}

manager@192.168.1.10 {"type": "joinGroup", "groupName": "group1"}

user2@192.168.1.10 {"type": "groupMembershipApproval", "approval": "yes", "user": "user2@192.168.1.10", "groupName": "group1"}

manager@192.168.1.10 {"type": "leaveGroup", "groupName": "group1"}

manager@192.168.1.11 {"type": "removeFromGroup", "groupName": "group2", "user": "user1@192.168.1.11"}

manager@192.168.1.11 {"type": "sendGroupMessage", "groupName": "group2", "text": "text group message"}

user1@192.168.1.11 {"type": "sendMessage", "text": "test personal message"}

user2@192.168.1.11 {"type": "transferGroupOwnership", "groupName": "group1"}

user1@192.168.1.11 {"type": "acceptGroupOwnership", "approval": "yes", "groupName": "group1"}

manager@192.168.1.11 {"type": "getGroupInfo", "groupName": "group1"}

user2@172.27.170.226 {"type": "profile", "username": "user2", "dob": "1/1/2012"}

user2@172.27.170.226 {"type": "viewProfile"}

user1@172.27.170.226 {"type": "getProfile"}

user2@172.27.170.226 {"type": "profileDetails"}

manager@172.27.170.226  {"type": "viewArchive"}
