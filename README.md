# configure_torch_aws


http://torch.ch/docs/getting-started.html   
following the insturciton above and when input the "th" from the terminal, one error got:   

-bash: th: command not found  


solution to fix this error:  
original when I went to the torch folder, there is no "install" folder. In order to resolve this I inputed the command:  
 ./update.sh   
 then I got the install.   
 
 
 and the following comand will active the th.   
 
  . ~/torch/install/bin/torch-activate

 Problem solved.  
 
 #  Run deepmask  
 
 error:
 
 /home/ec2-user/torch/install/bin/luajit: /home/ec2-user/torch/install/share/lua/5.1/trepl/init.lua:389: /home/ec2-user/torch/install/share/lua/5.1/trepl/init.lua:389: /home/ec2-user/torch/install/share/lua/5.1/cudnn/ffi.lua:1603: 'libcudnn (R5) not found in library path.

 
 solution:  
  export LD_LIBRARY_PATH=/usr/local/cuda/lib64/



error:  

/home/ec2-user/torch/install/bin/luajit: cannot open </pretrained/deepmask/model.t7> in mode r  at /home/ec2-user/torch/pkg/torch/lib/TH/THDiskFile.c:670
stack traceback:
        [C]: at 0x7fd6ce4b32c0
        [C]: in function 'DiskFile'
        /home/ec2-user/torch/install/share/lua/5.1/torch/File.lua:405: in function 'load'
        computeProposals.lua:49: in main chunk
        [C]: in function 'dofile'
        ...user/torch/install/lib/luarocks/rocks/trepl/scm-1/bin/th:151: in main chunk
        [C]: at 0x004064c0



solution:
luarocks install json

json is not installed so I got the error.
