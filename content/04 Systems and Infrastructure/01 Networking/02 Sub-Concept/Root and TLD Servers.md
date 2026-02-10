# Root and TLD Servers

> <- Back to [[Resolution Process]]

Root name servers (13 logical servers, hundreds of physical instances via anycast) direct queries to the appropriate TLD (Top-Level Domain) servers (.com, .org, .io, etc.). TLD servers then direct to the authoritative servers for the specific domain. This hierarchical delegation distributes DNS load globally.

#networking #dns
