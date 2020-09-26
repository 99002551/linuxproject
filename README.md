# linuxproject

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/0b804cf439af4b7bb9b8e60ef67ef920)](https://app.codacy.com/manual/99002551/linuxproject?utm_source=github.com&utm_medium=referral&utm_content=99002551/linuxproject&utm_campaign=Badge_Grade_Settings)name: cppcheck-action
on: [push]

jobs:
  build:
    name: cppcheck
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
        
      - name: Install cppcheck
        run: sudo apt-get -y install cppcheck
      - name: Cppcheck code
        run: cppcheck MiniProject_C/3_Implementation 

