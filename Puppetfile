# Warning: This file is managed by puppet.
# 
# Please look at the Puppetfile-cambridge module and files for information
#
#
# This Logic was provided by bodepd

# the account where the Openstack modules should come from
#
#

# this modulefile has been configured to use two sets of repos.
# the account where the Openstack modules should come from
#
# this file also accepts a few environment variables
#
git_protocol=ENV['git_protocol'] || 'git'

#
# this modulefile has been configured to use two sets of repos.
# The downstream repos that Cisco has forked, or the upstream repos
# that they are derived from (and should be maintained in sync with)
#

#
# this is just targeting the upstream stackforge modules
# right now, and the logic for using downstream does not
# work yet
#

if ENV['repos_to_use']  == 'downstream'
  # this assumes downstream which is the Cisco branches
  branch_name               = 'origin/havana'
  openstack_module_branch   = branch_name
  openstack_module_account  = 'CiscoSystems'
  puppetlabs_module_account = 'CiscoSystems'
  # manifests
  user_name = 'CiscoSystems'
  release = 'havana'
  manifest_branch = 'origin/multi-node'
else
  # use the upstream modules where they exist
  branch_name               = 'origin/havana'
  openstack_module_branch   = 'master'
  openstack_module_account  = 'stackforge'
  puppetlabs_module_account = 'puppetlabs'
  # manifests
  user_name = 'primeministerp'
  release = 'havana'
  manifest_branch = 'origin/master'
end

base_url     = "#{git_protocol}://github.com"
ssh_url      = "#{git_protocol}://github.com"
branch_name  = 'origin/havana'

###### Installer Manifests Example ##############
#mod 'manifests', :git => "#{base_url}/#{user_name}/#{release}-manifests", :ref => "#{manifest_branch}"

##### Puppet Labs modules #####

openstack_repo_prefix = "#{base_url}/#{openstack_module_account}/puppet"
mod 'windows_sql',        :git => "#{base_url}/insentia/windows_sql" #TESTING
mod 'windows_sharepoint', :git => "#{base_url}/insentia/windows_sharepoint" #TESTING
mod 'windows_ad',         :git => "#{base_url}/insentia/windows_ad" #TESTING
mod 'windows_services',   :git => "#{base_url}/insentia/windows_services" #TESTING
mod 'windows_isos',       :git => "#{base_url}/insentia/windows_isos" #TESTING
mod 'networkdevice', :git => "#{base_url}/uniak/puppet-networkdevice" #TESTING
#mod 'mariadb',      :git => "#{base_url}/NeCTAR-RC/puppet-mariadb" #TESTING
mod 'galera',        :git => "#{base_url}/CiscoSystems/puppet-galera" #TESTING
mod 'r10k',                       :git => "#{base_url}/acidprime/r10k" #TESTING
mod 'transport',        :git => "#{base_url}/nanliu/puppet-transport",        :ref => 'master' #TESTING
mod 'lsb',              :git => "#{base_url}/nanliu/puppet-lsb",              :ref => 'master' #TESTING
#mod 'git',              :git => "#{base_url}/nanliu/puppet-git",              :ref => 'master' #TESTING
mod 'export_resources', :git => "#{base_url}/nanliu/puppet-export_resources", :ref => 'master' #TESTING
mod 'hiera',           	:git => "#{base_url}/nanliu/puppet-hiera",            :ref => 'master' #TESTING
mod 'archive',        	:git => "#{base_url}/nanliu/puppet-archive",	      :ref => 'master' #TESTING
#mod 'winrm',  	        :git => "#{base_url}/nanliu/puppet-winrm",            :ref => 'master' #TESTING
mod 'gitlab',              :git => "#{ssh_url}/openstack-hyper-v/puppet-gitlab" #TESTING
mod 'gitlab_server',       :git => "#{ssh_url}/openstack-hyper-v/puppet-gitlab_server" #TESTING
mod 'win-cis',           :git => "#{base_url}/rismoney/puppet-win-cis" #TESTING
mod 'baremetal-windows', :git => "#{base_url}/rismoney/puppet-baremetal-windows" #TESTING
mod 'wsus',              :git => "#{base_url}/rismoney/puppet-wsus" #TESTING
mod 'windowsnetwork',    :git => "#{base_url}/rismoney/puppet-windowsnetwork" #TESTING
mod 'winclusters',       :git => "#{base_url}/rismoney/puppet-winclusters" #TESTING
mod 'winsvc',            :git => "#{base_url}/rismoney/puppet-winsvc" #TESTING
mod 'iis',               :git => "#{base_url}/rismoney/puppet-iis" #TESTING
