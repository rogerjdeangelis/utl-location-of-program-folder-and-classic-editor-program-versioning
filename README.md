# utl-location-of-program-folder-and-classic-editor-program-versioning
Location of Program folder and classic editor program versioning  
    Location of Program folder and classic editor program versioning                                                      
                                                                                                                          
    You should always know where your progam and the previous versions are located.                                       
                                                                                                                          
    github                                                                                                                
    https://tinyurl.com/y49ob43p                                                                                          
    https://github.com/rogerjdeangelis/utl-location-of-program-folder-and-classic-editor-program-versioning               
                                                                                                                          
    SAS Forum  (related to - I don't use other editors)                                                                   
    https://tinyurl.com/y6koh3fr                                                                                          
    https://communities.sas.com/t5/SAS-Enterprise-Guide/obtain-current-program-path-from-saseg-4-3/m-p/674992             
                                                                                                                          
    /*                                                                                                                    
                                                                                                                          
    determine present program working directory                                                                           
                            _                                                                                             
     _ __  _ ____      ____| |                                                                                            
    | `_ \| `_ \ \ /\ / / _` |                                                                                            
    | |_) | |_) \ V  V / (_| |                                                                                            
    | .__/| .__/ \_/\_/ \__,_|                                                                                            
    |_|   |_|                                                                                                             
    */                                                                                                                    
                                                                                                                          
    To answer the ops question                                                                                            
                                                                                                                          
    The present program working directory(ppwd) is located at                                                             
                                                                                                                          
    filename pwd "./";                                                                                                    
    %put -- %sysfunc(pathname(pwd)) --;                                                                                   
                                                                                                                          
    -- c:\utl --                                                                                                          
                                                                                                                          
    /*                  _             _                                                                                   
    __   _____ _ __ ___(_) ___  _ __ (_)_ __   __ _                                                                       
    \ \ / / _ \ `__/ __| |/ _ \| `_ \| | `_ \ / _` |                                                                      
     \ V /  __/ |  \__ \ | (_) | | | | | | | | (_| |                                                                      
      \_/ \___|_|  |___/_|\___/|_| |_|_|_| |_|\__, |                                                                      
                                              |___/                                                                       
    */                                                                                                                    
                                                                                                                          
                                                                                                                          
    Versioning Local power workstation (classic editor is required?)                                                      
                                                                                                                          
    At any time, if you push the 'middle mouse button' or function key 1, a timestamped verison of your program           
    will be saved in your versionaing folder(c:/ver and your program folder).                                             
                                                                                                                          
    How to version your SAS code                                                                                          
                                                                                                                          
      1. Assign a triple letter token to your project. I will use 'dms'.                                                  
                                                                                                                          
      2. On the SAS icon populate the 'start-in' field with the location of your programs                                 
         I use 'c:/utl'                                                                                                   
         All your code will be saved in 'c:/utl'. All project programs have                                               
         mutally exclusive names, because they have the project prefix.                                                   
         I have all my programs over the last 40 years in c:/utl.                                                         
                                                                                                                          
             dms_100nit.sas  - intialization program                                                                      
             dms_200get.sas  - get data program                                                                           
                                                                                                                          
      3. Create 'c:/ver' to save versions of your sas code.                                                               
                                                                                                                          
      4. insert this line in your  autoexec file  (c:/oto/dms_oto.sas)                                                    
         %Let _q=%sysfunc(int(%sysfunc(time())));                                                                         
                                                                                                                          
      5. When SAS comes up make sure you are in the classic editor not EE or EG                                           
         see https://studio.youtube.com/video/dvDjfIRciB8/edit/basic?o=U                                                  
             https://studio.youtube.com/video/e0V8zg7Y4X8/edit/basic?o=U                                                  
                                                                                                                          
      6. Type this on the first line of the classic editor                                                                
         %let pgm=dms_100nit;                                                                                             
         Then type subtop on the command line. (or just right mouse button)                                               
                                                                                                                          
      7. Type 'keys' on the clean command line (do not use the command line in EE?)                                       
         Type this text on the function key PF1. You can no longer copy/paste.                                            
                                                                                                                          
         pgm;file &pgm..sas;file c:\ver\&pgm.&_q..sas;%let _q=%eval(0&_q +1);                                             
                                                                                                                          
         I think a lot of functionality was lost wit the C rewrite of SAS.                                                
                                                                                                                          
     Now if you push the MMB or PF1 a timestammed version will be saved in c:/ver                                         
                                                                                                                          
    /*        __                                                                                                          
    (_)_ __  / _| ___                                                                                                     
    | | `_ \| |_ / _ \                                                                                                    
    | | | | |  _| (_) |                                                                                                   
    |_|_| |_|_|  \___/                                                                                                    
                                                                                                                          
    */                                                                                                                    
                                                                                                                          
    SAS Forum                                                                                                             
    https://tinyurl.com/y6koh3fr                                                                                          
    https://communities.sas.com/t5/SAS-Enterprise-Guide/obtain-current-program-path-from-saseg-4-3/m-p/674992             
                                                                                                                          
    Youtube                                                                                                               
    https://tinyurl.com/y2yegvpn                                                                                          
                                                                                                                          
    github repos                                                                                                          
    https://tinyurl.com/y3jllyb4                                                                                          
    https://github.com/rogerjdeangelis?tab=repositories&q=classic+editor&type=&language=                                  
    https://github.com/rogerjdeangelis/utl_classic_sas_editor_display_manager_commands_improved                           
    https://github.com/rogerjdeangelis/utl_classic_editor_part_II                                                         
    https://studio.youtube.com/video/e0V8zg7Y4X8/edit/basic?o=U                                                           
    https://www.youtube.com/watch?v=X1D6SdOwF2g                                                                           
                                                                                                                          
                                                                                                                          
                                                                                                                          
