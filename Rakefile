task :default => :serve

task :serve do
  require 'webrick'

  server = WEBrick::HTTPServer.new(:Port => 8000, :DocumentRoot => '.')

  begin
    trap 'SIGINT' do
      server.stop
    end

    server.start
  ensure
    server.stop
  end
end
