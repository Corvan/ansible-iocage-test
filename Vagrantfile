Vagrant.configure("2") do |config|
  config.vm.box = "punktde/freebsd-120-zfs"
  config.vm.box_version = "12.0.5"
  config.vm.synced_folder '.', '/vagrant', id: 'vagrant-root', disabled: true
end
