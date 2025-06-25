#EEE README – Εκτέλεση Ansible Playbooks

## 1. Προϋποθέσεις

• Ansible εγκατεστημένο στο control machine  
• Ορισμένο αρχείο inventory (π.χ. `hosts.yaml`)  
• SSH πρόσβαση στα target VMs με τον χρήστη `azureuser`  
• Τα playbooks (`spring.yaml`, `postgres.yaml`, κ.λπ.) και τα templates στον ίδιο φάκελο

## 2. Εκτέλεση Playbooks

### Βήμα 1: Εγκατάσταση και ρύθμιση PostgreSQL

```bash
ansible-playbook -i hosts.yaml postgres.yaml
```

### Βήμα 2: Deploy Spring Boot εφαρμογής + nginx reverse proxy

```bash
ansible-playbook -i hosts.yaml spring.yaml
```


