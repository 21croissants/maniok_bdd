# More info at https://github.com/guard/guard#readme

guard 'rspec' do
  watch(%r{^spec/unit/.+_spec\.rb$})
  watch(%r{^lib/(.+)\.rb$})     { |m| "spec/unit/#{m[1]}_spec.rb" }
  watch('spec/unit/spec_helper.rb')  { "spec/unit" }
end

guard 'cucumber', cli: "--profile guard" do
  watch(%r{^features/.+\.feature$})
  watch(%r{^spec/acceptance/cucumber/support/.+$})          { 'features' }
  watch(%r{^spec/acceptance/cucumber/step_definitions/(.+)_steps\.rb$}) { |m| Dir[File.join("**/#{m[1]}.feature")][0] || 'features' }
end
