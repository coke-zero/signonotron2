#!/usr/bin/env rake
# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require File.expand_path('../config/application', __FILE__)

require_relative 'lib/volatile_lock'
include VolatileLock::DSL

Signonotron2::Application.load_tasks

task :default => [:test, :spec, :check_for_bad_time_handling, 'jasmine:ci']
