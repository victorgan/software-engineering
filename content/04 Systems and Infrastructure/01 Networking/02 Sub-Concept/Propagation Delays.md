# Propagation Delays

> <- Back to [[TTL]]

When DNS records are changed, the old records remain in caches until their TTL expires. This means changes are not instant — different users see different results depending on when their resolver last cached the record. Full propagation can take up to the previous TTL duration. This is why lowering TTL before a migration is important.

#networking #dns
