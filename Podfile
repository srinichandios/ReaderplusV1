# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

source 'https://github.com/PearsonTech/ios-readerplus-podspecs.git'
source 'https://github.com/cocoaPods/Specs.git'

target 'Readerplus' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!
  pod 'GLSApiKit', '~> 0.6.0'
  #pod 'Authentication', :git => 'ssh://git@bitbucket.pearson.com/mobi/authentication-sdk.git', :branch => 'Swift-4.2'
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '4.2'
      target.build_settings(config.name)['CLANG_ALLOW_NON_MODULAR_INCLUDES_IN_FRAMEWORK_MODULES'] = 'YES'
    end
  end
end
