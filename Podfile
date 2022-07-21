source 'https://github.com/CocoaPods/Specs.git'

use_frameworks!

target 'PEPE_TEST' do
  platform :ios, '12.4'

  # Pods for PEPE_TEST
    pod 'RealmSwift', '10.28.2', :inhibit_warnings => true
end

target 'PEPE_TEST_WATVH Watch App' do
  platform :watchos, '5.3'
  # Pods for PEPE_TEST_WATVH Watch App

    pod 'RealmSwift', '10.28.2', :inhibit_warnings => true
end

post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            if config.name == 'Release'
                config.build_settings['SWIFT_OPTIMIZATION_LEVEL'] = '-Owholemodule'
            else
                config.build_settings['SWIFT_OPTIMIZATION_LEVEL'] = '-Onone'
            end
        end
    end
end
