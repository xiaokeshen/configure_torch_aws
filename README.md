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



