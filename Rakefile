require 'date'

SHA_SHORT=%x[git rev-parse --short HEAD].chomp
DATE=DateTime.now.strftime("%y%m%d")

TAG="D#{DATE}G#{SHA_SHORT}"
BRANCH="DAWN-2018-04-27-ALPHA"


task :build do
    sh %[docker build --build-arg BRANCH=#{BRANCH} . -t eosamsterdam/eos:#{BRANCH}]
end

task :push do
    sh %[docker push eosamsterdam/eos:#{BRANCH}]
end
