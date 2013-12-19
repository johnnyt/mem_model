# -*- ruby -*-

#require 'rubygems'
require 'hoe'

Hoe.plugin :git
Hoe.plugin :gemspec

Hoe.spec 'mag_model' do
  developer 'JohnnyT', 'ubergeek3141@gmail.com'

  self.summary     = 'ActiveModel-compliant MagLev persistence'
  self.description = <<-DESC.strip.gsub(/\n\s+/, " ")
    MagModel persists Ruby objects using MagLev as a data storage engine. It's an
    ActiveModel implementation so it works stand-alone or in Rails 3 as a drop-in
    replacement for ActiveRecord or DataMapper.  If MagModel is used in non-MagLev
    platforms, objects will be persisted to in-memory sets.
  DESC
  self.urls        = ['https://github.com/johnnyt/mag_model']

  self.history_file = 'CHANGELOG.md'
  self.readme_file  = 'README.md'
  self.testlib      = :minitest

  license 'MIT'

  dependency 'active_attr',    '>= 0.8.2'
  dependency 'activesupport',  '= 3.2.15' # MagLev optimized version
end

Dir['tasks/**/*.rake'].each { |t| load t }

# vim: syntax=ruby