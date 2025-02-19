![image](https://github.com/user-attachments/assets/1b362fae-b394-4d90-8172-7edb00c1502b)
![image](https://github.com/user-attachments/assets/a4da4332-bd45-4c3e-b4eb-91acc0b1d942)

The first step is to create SSH key pairs to connect to the AWS instances that Terraform will create. This can be done with the following command

```
ssh-keygen -t rsa
```

Use the following command to push changes from your Ansible:

```
ansible-playbook playbook.yml
```

### A breakdown of the playbook:

```
  # this begins the tasks block
  tasks:
    # name will define the name of the first task. Task names must be unique
    - name: Install nginx
      # This line will identify the module being used. In this case, it is package
      ansible.builtin.package:
        # these lines of code will tell the remote host to install the latest package of nginx
        name: nginx
        state: latest
```
