# tripleo-latency-tests

To add latency:
for nic in br-ex vlan10 vlan20 vlan30 vlan40 vlan50; do echo $nic; tc qdisc del dev $nic root netem; tc qdisc add dev $nic root netem delay 300ms; done

Need to do this in both directions
