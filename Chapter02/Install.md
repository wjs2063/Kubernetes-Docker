virtual box install

https://www.virtualbox.org/wiki/Download_Old_Builds_6_1
아마 m1 mac 에서는 1908 에러가 뜰것이고 ( 아직 지원을 하지않는것같음 )
window 에서는


failed to get device handle and/or partition id for 00000000016f3190 (hpartitiondevice=0000000000000d25, last=0xc0000002/1) (verr_nem_vm_create_failed)
해당 에러가 뜰수도있다.

침착하게 


관리자 모드로 cmd 창 켜고

```
bcdedit /set hypervisorlaunchtype off

```


```
shutdown -s -t 2
```

그리고 virtual box 실행 하면 ok

```
brew install vagrant
```




```
vagrant init
```
- 정상 - 
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.


vagrant Cloud 페이지 :  https://app.vagrantup.com/sysnet4admin/boxes/CentOS-k8s

vagrantfile :   config.vm.box = "sysnet4admin/CentOS-k8s" 수정하기 

```
vagrant up
```
default: Successfully added box 'sysnet4admin/CentOS-k8s' (v0.7.4) for 'virtualbox 메세지가 나오면 성공




