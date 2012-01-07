require 'digest/md5'

DEFAULT_PASS = 'deadbeef'

namespace :cre_loaded do
  desc 'Calculate CRE Loaded suitable password hash'
  task '6.1', [:pass] do |t, args|
    args.with_defaults(:pass => DEFAULT_PASS)
    puts "CRE Loaded hash for password '#{args.pass}'"
    puts Digest::MD5.new.hexdigest("69#{args.pass}") + ':69'
  end
end

namespace :joomla do
  desc 'Calculate Joomla passwor hash'
  task '1.5', [:pass] do |t, args|
    args.with_defaults(:pass => DEFAULT_PASS)
    puts "Joomla hash for password '#{args.pass}'"
    puts Digest::MD5.new.hexdigest("#{args.pass}00000000000000000000000000000000") + ':00000000000000000000000000000000'
  end
end

# vim:ts=2:sw=2
