# Python cookbook
## Requirements
Provision a machine with a python cookbook we created.

### Unit tests for:

- Python version installed
- Pip version installed
- The dependency libncurses5-dev will install

### Integration tests for:

- Version install match
- pip install
- libncurses5-dev install

### How to use
- In your projects Berksfile, include this line:
``cookbook "python", git: "git@github.com:Els-Sparta/PythonCookbook.git" ``
- Run this line in your console:
berks vendor cookbooks
- This cookbook is now ready to provision!

Don't forget if you're using vagrant, add in your Vagrantfile:
``config.vm.provision("chef_solo") do |chef|
    chef.add_recipe("python::default")
  end
``
