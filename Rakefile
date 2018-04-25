task :default => :compile  do
  sh 'echo "a=b=c=2<3;" | ./a.out'
end

task :while => :compile do
  sh 'echo "{ i=1; while (i<100) i=i+i; }" | ./a.out'
  sh 'echo "{ i=125; j=100; while (i-j) if (i<j) j=j-i; else i=i-j; }" | ./a.out'
  sh 'echo "{ i=1; do i=i+10; while (i<50); }" | ./a.out'
  sh 'echo "{ i=1; while ((i=i+10)<50) ; }" | ./a.out'
  sh 'echo "{ i=7; if (i<5) x=1; if (i<10) y=2; }" | ./a.out'
end


task :compile do
  sh "gcc tiny.c"
end
