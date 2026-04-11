# linux_patching
An ansible playbook that will patch generic debian based OSs.
This playbook will also patch debian based nodes in a kubernetes cluster assuming you have setup your inventory correctly(see example inventory)

If you are patching kubernetes nodes you will also need to pass in the var `k8s_control_node`
You will also need to install the [kubernetes.core collection](https://galaxy.ansible.com/ui/repo/published/kubernetes/core/?extIdCarryOver=true&sc_cid=RHCTG0180000371695) as well as the requirements it needs.

Example of how to run this playbook
`ansible-playbook -i inventory.yml main.yml -e "k8s_control_node=kubecon01.domain.local" -K`
