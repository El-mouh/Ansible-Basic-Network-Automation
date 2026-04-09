# Ansible Network Automation Project

## 📌 Overview

This project automates Cisco IOS routers using Ansible.

It configures:

* Interfaces (IP address, description, state)
* Static routes
* Verification of configuration
* Saves output to files

---

## 📂 Project Structure

```
ansibledir/
├── inventory/
│   ├── group_vars/
│   ├── host_vars/
│   └── hosts.ini
├── outputs/
├── playbook.yml
```

---

## ▶️ How to Run

Run the full playbook:

```
ansible-playbook -i inventory/ playbook.yml
```

---

## 🎯 Run Specific Tasks (using tags)

Run only interface configuration:

```
ansible-playbook -i inventory/ playbook.yml --tags interfaces
```

Run only IP configuration:

```
ansible-playbook -i inventory/ playbook.yml --tags l3_interfaces
```

Run only static routes:

```
ansible-playbook -i inventory/ playbook.yml --tags static_routes
```

Run only verification:

```
ansible-playbook -i inventory/ playbook.yml --tags verify
```

---

## 📥 Outputs

After execution, device outputs are saved in:

```
outputs/
```

Example:

```
R1_interfaces.txt
R1_routes.txt
```

---

## 🖥️ Devices

* R1
* R2
* R3

---

## ⚠️ Notes

* Make sure SSH is enabled on devices
* Ensure correct credentials in inventory
* Designed for Cisco IOS (CML / GNS3 / EVE-NG)

---

## 🚀 Future Improvements

* Add OSPF automation
* Add config validation
* Use Jinja2 templates
