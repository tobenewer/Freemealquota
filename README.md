# Freemealquota
Freemealquota

---Free meal quota generation 20200429
update [wfcpdb].[dbo].ktc_freemealquota
         set fld_dsun = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                              then fld_lastrunresult 
							  else fld_dsun end ),
	         fld_dmon = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
                              then fld_lastrunresult  
							  else fld_dmon end ),
			 fld_dtue = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
                              then fld_lastrunresult 
							  else fld_dtue  end ),
			 fld_dwed = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
                              then fld_lastrunresult 
							  else fld_dwed  end ),
	         fld_dtur = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
                              then fld_lastrunresult 
							  else fld_dtur  end ),
			 fld_dfri = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
                              then fld_lastrunresult 
							  else fld_dfri  end ),
			 fld_dsat = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
                              then fld_lastrunresult 
							  else fld_dsat  end ),

			fld_dsuna = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                              then fld_lastrunresulta 
							  else fld_dsuna end ),
	         fld_dmona = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
                              then fld_lastrunresulta  
							  else fld_dmona end ),
			 fld_dtuea = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
                              then fld_lastrunresulta 
							  else fld_dtuea  end ),
			 fld_dweda = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
                              then fld_lastrunresulta 
							  else fld_dweda  end ),
	         fld_dtura = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
                              then fld_lastrunresulta 
							  else fld_dtura  end ),
			 fld_dfria = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
                              then fld_lastrunresulta 
							  else fld_dfria  end ),
			 fld_dsata = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
                              then fld_lastrunresulta 
							  else fld_dsata  end ),

			fld_dsunb = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                              then fld_lastrunresultb 
							  else fld_dsunb end ),
	         fld_dmonb = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
                              then fld_lastrunresultb  
							  else fld_dmonb end ),
			 fld_dtueb = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
                              then fld_lastrunresultb 
							  else fld_dtueb  end ),
			 fld_dwedb = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
                              then fld_lastrunresultb 
							  else fld_dwedb  end ),
	         fld_dturb = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
                              then fld_lastrunresultb 
							  else fld_dturb  end ),
			 fld_dfrib = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
                              then fld_lastrunresultb 
							  else fld_dfrib  end ),
			 fld_dsatb = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
                              then fld_lastrunresultb 
							  else fld_dsatb  end )
		 where CONVERT(varchar(100), fld_ddate, 23) 
                    >= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                 and  CONVERT(varchar(100), fld_ddate, 23) 
                    <= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23) 

--set the delta value to be 0 for records before current date after the period start date 20200508 Do NOT retro calculate the meal quota

update [wfcpdb].[dbo].ktc_freemealquota
         set  fld_delta  = 0
		     ,fld_deltab = 0
			 ,fld_deltaa = 0
		where  CONVERT(varchar(100), fld_ddate, 23) 
                    >= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) 
		   and CONVERT(varchar(100), fld_ddate, 23) 
                    < CONVERT(nvarchar(10), getdate(),23)


--set the delta value to be 0 for records before current date after the period start date 20200508 Do NOT retro calculate the meal quota

----------------------------------------------------------------------------------------------------------------------
 --update delta quota start
 update [wfcpdb].[dbo].ktc_freemealquota
        set fld_personnum = dailymeal1.PERSONNUM, 
            fld_quotatype= dailymeal1.mtype, 
            fld_ddate = dailymeal1.SHIFTSTARTDATE, 
            fld_expdate = dailymeal1.expdate, 
            fld_shiftlength = dailymeal1.shifttotal, --????don't update the old data????????????????????????
            fld_lastrunresult = dailymeal1.dailymealquota, --????don't update the old data????????????????????????
			fld_lastrunresulta = dailymeal1.packagea,  --20200507 different package
			fld_lastrunresultb = dailymeal1.packageb,  --20200507 different package
            fld_lastrundate =  CONVERT(nvarchar(10), getdate(),23), --????don't update the old data????????????????????????
            fld_weekstartdate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23),  --????don't update the old data?????????????????????
            fld_delta = dailymeal1.dailymealquota -  (
                 case when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                          then ktc_freemealquota.fld_dsun
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
                          then ktc_freemealquota.fld_dmon
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
                          then ktc_freemealquota.fld_dtue
                      when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
                          then ktc_freemealquota.fld_dwed
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
                          then ktc_freemealquota.fld_dtur
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
                          then ktc_freemealquota.fld_dfri
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
                          then ktc_freemealquota.fld_dsat
	                  else 0  end ),
			fld_deltaa = dailymeal1.packagea -  (
                 case when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                          then ktc_freemealquota.fld_dsuna
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
                          then ktc_freemealquota.fld_dmona
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
                          then ktc_freemealquota.fld_dtuea
                      when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
                          then ktc_freemealquota.fld_dweda
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
                          then ktc_freemealquota.fld_dtura
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
                          then ktc_freemealquota.fld_dfria
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
                          then ktc_freemealquota.fld_dsata
	                  else 0  end ),
			fld_deltab = dailymeal1.packageb -  (
                 case when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                          then ktc_freemealquota.fld_dsunb
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
                          then ktc_freemealquota.fld_dmonb
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
                          then ktc_freemealquota.fld_dtueb
                      when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
                          then ktc_freemealquota.fld_dwedb
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
                          then ktc_freemealquota.fld_dturb
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
                          then ktc_freemealquota.fld_dfrib
	                  when fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
                          then ktc_freemealquota.fld_dsatb
	                  else 0  end )
		    /* fld_dsun = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                              then dailymeal1.dailymealquota end ),
	         fld_dmon = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
                              then dailymeal1.dailymealquota end ),
			 fld_dtue = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
                              then dailymeal1.dailymealquota end ),
			 fld_dwed = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
                              then dailymeal1.dailymealquota end ),
	         fld_dtur = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
                              then dailymeal1.dailymealquota end ),
			 fld_dfri = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
                              then dailymeal1.dailymealquota end ),
			 fld_dsat = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
                              then dailymeal1.dailymealquota end )*/
from 
     ( 
	 /*delta daily start*/
	    select detail.personnum
              ,'daily' as mtype
	          ,CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 23) SHIFTSTARTDATE
	          ,CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, 0, CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 23)) ), 6),121) as expdate  --??need to generate based on the shift start date
	          ,sum(detail.shifthours) as shifttotal
	          ,case  when sum(detail.shifthours) < '4' then 0  
 					 when sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6' then 1   
					 when sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12' then 2  
					 when sum(detail.shifthours) >= '12'  then 3 
 					 else 0 end as dailymealquota 
			 ,case  when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '22:00:00' or min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '10:00:00' and CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '22:00:00' ) 
			              then  2*/
					 when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '22:00:00' or min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '02:00:00' ) 
			              then  2
                     when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '02:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '10:00:00' and CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '22:00:00' ) 
			              then  5*/
					 when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '20:00:00' ) 
			              then  1
                     when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '20:00:00' or  min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  2 
					 else 0 end as packagea
             ,case  /*when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '22:00:00' or CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '10:00:00' ) 
			              then  1*/
					 when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '22:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '22:00:00' or CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '02:00:00' ) 
			              then  3*/
                     when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '02:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					 when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '22:00:00' ) 
			              then  2
					 when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '20:00:00' ) 
			              then  2
                     when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '20:00:00' or  min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1 
					 else 0 end as packageb
        from (
             SELECT --[SHIFTASSIGNID]
                    --,[EMPLOYEEID]
	                person.personnum
                    -- ,[SHIFTID]
	                ,[ENTEREDONDTM]
	                ,[SHIFTSTARTDATE]
	                ,[SHIFTENDDATE]
	                ,datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) as shifthours
	                /*, case  when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '4' then 0  

					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '4'  and datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '6' then 1   
					
					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '6'  and datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '12' then 2  
					
					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '12'  then 3 
						
					else 0 end as mealquota */    
             FROM [wfcpdb].[dbo].[SHIFTASSIGNMNT]
                 join [wfcpdb].[dbo].shiftcode on shiftcode.shiftcodeid = SHIFTASSIGNMNT.shiftcodeid
                 join [wfcpdb].[dbo].person on person.personid = shiftassignmnt.employeeid  
             where     
                 CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
                     >= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) --???change it to be the current date if the interface run after 00:00
                     -->= CONVERT(nvarchar(10), getdate(),23)
				 and  CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
                    <= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23) 
                 and shiftassignmnt.[DELETEDSW] <> '1'
                 and (shiftcode.paycodeid  not in ( '128' , '102' , '138') or shiftcode.paycodeid is null) --?need to add the pay code?
              ) detail
              group by personnum,  CONVERT(varchar(100), [SHIFTSTARTDATE], 23) 

	   /*delta daily end*/
 -- ***********************************************************************
--/*           
union
	  /*delta weekly start*/
           select 
                dailymeal.personnum
                ,'weekly' mtype
                ,dailymeal.weekstartdate as shiftstartdate
                --, CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 6),121) as expdate
                ,CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, 0, dailymeal.weekstartdate) ), 6),121) as expdate  --??need to generate based on the shift start date
                ,sum(dailymeal.shifttotal) as shifttotal
                ,sum (dailymeal.dailymealquota) as dailymealquota
				,sum(dailymeal.packagea) as packagea --2020.05.07
				,sum(dailymeal.packageb) as packageb --2020.05.07
            from(
                select detail.personnum
                      ,'daily' as mtype
	                  ,CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),121) weekstartdate
                      -- ,detail.ENTEREDONDTM
	                  ,CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 23) SHIFTSTARTDATE
	                  -- ,CONVERT(varchar(100), detail.SHIFTENDDATE, 23) SHIFTENDDATE
	                  ,sum(detail.shifthours) as shifttotal
	                  --,detail.mealquota
	                  ,case  when sum(detail.shifthours) < '4' then 0  

					         when sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6' then 1   
					
					         when sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12' then 2  
					
					         when sum(detail.shifthours) >= '12'  then 3 
						
					         else 0 end as dailymealquota 
					,case  when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '22:00:00' or min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			                    then  1
					      /* when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '10:00:00' and CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '22:00:00' ) 
			                    then  2*/
					      when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '22:00:00' or min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '02:00:00' ) 
			                    then  2
                          when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '02:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			                    then  1
					     /* when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '10:00:00' and CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '22:00:00' ) 
			                    then  5*/
					      when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '20:00:00' ) 
			                    then  1
                          when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '20:00:00' or  min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			                    then  2 
						  else 0 end as packagea
                   ,case  /*when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '22:00:00' or CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '10:00:00' ) 
			                    then  1*/
					      when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '22:00:00' ) 
			                    then  1
					    /* when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '22:00:00' or CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '02:00:00' ) 
			                    then  3*/
                          when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '02:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			                    then  1
					      when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '22:00:00' ) 
			                    then  2
					      when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '20:00:00' ) 
			                    then  2
                          when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '20:00:00' or  min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			                    then  1 
						  else 0 end as packageb
               from (
                     SELECT --[SHIFTASSIGNID]
                            --,[EMPLOYEEID]
	                        person.personnum
                            -- ,[SHIFTID]
	                        ,[ENTEREDONDTM]
	                        ,[SHIFTSTARTDATE]
	                        ,[SHIFTENDDATE]
	                        , datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) as shifthours
	                        /*, case  when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '4' then 0  

					        when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '4'  and datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '6' then 1   
					
					        when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '6'  and datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '12' then 2  
					
					        when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '12'  then 3 
						
					        else 0 end as mealquota */
                     FROM [wfcpdb].[dbo].[SHIFTASSIGNMNT]
                          join [wfcpdb].[dbo].shiftcode on shiftcode.shiftcodeid = SHIFTASSIGNMNT.shiftcodeid
                          join [wfcpdb].[dbo].person on person.personid = shiftassignmnt.employeeid
                          -- where shiftcode.shiftcodeid in ('413' , '401', '407','411','404') and shiftcode.paycodeid = '137' and deletedsw <> '1'
                     where   
                          --[ENTEREDONDTM] = getdate()
                          -- CONVERT(varchar(100), [ENTEREDONDTM], 23) = CONVERT(varchar(100), getdate(), 23) 
                          CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
                             >= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) --???change it to be the current date if the interface run after 00:00
                             -->= CONVERT(nvarchar(10), getdate(),23)
                          and  CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
                             <= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23) 
                          and shiftassignmnt.[DELETEDSW] <> '1'
                          and (shiftcode.paycodeid  not in ( '128' , '102', '138' ) or shiftcode.paycodeid is null)
                     --group by CONVERT(varchar(100), [SHIFTSTARTDATE], 23)
                     --order by shiftstartdate
                      ) detail
                      group by personnum,  CONVERT(varchar(100), [SHIFTSTARTDATE], 23) ) dailymeal
              group by personnum, dailymeal.weekstartdate 
			 -- */  /*delta weekly end*/  
			  ) dailymeal1
			 
     where     fld_personnum = dailymeal1.PERSONNUM 
	      and  fld_quotatype= dailymeal1.mtype 
		  and  fld_ddate = dailymeal1.SHIFTSTARTDATE  
		  and  fld_expdate = dailymeal1.expdate
		  and  fld_ddate >= CONVERT(nvarchar(10), getdate(),23) -- 20200508 only update the data from today
	
	/*and  CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
                             >= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                          and  CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
                             <= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23) */   --20200507 check the update period.


 --update delta quota end


 --initial quota creation start

insert into [wfcpdb].[dbo].ktc_freemealquota 
            (fld_personnum, 
            fld_weekstartdate, 
            fld_quotatype, 
            fld_ddate, 
            fld_expdate, 
            fld_lastrundate, 
            fld_shiftlength,
            /*fld_dsun,
            fld_dmon,
            fld_dtue,
            fld_dwed,
            fld_dtur,
            fld_dfri,
            fld_dsat,*/
			fld_lastrunresult,
			fld_lastrunresulta,
			fld_lastrunresultb,
			fld_delta,
			fld_deltaa,
			fld_deltab)

select   allshift.pid,
         allshift.weekstartdate,
	     allshift.quotatype,
	     allshift.SHIFTSTARTDATE,
	     allshift.expdate,
	     allshift.lastrundate,
	     allshift.shifttotal,
	     /*case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
             then allshift.dailymealquota end as dsun, 
	     case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
             then allshift.dailymealquota end as dmon,
	     case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
             then allshift.dailymealquota end as dtue,
         case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
             then allshift.dailymealquota end as dwed,
	     case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
             then allshift.dailymealquota end as dtur,
	     case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
             then allshift.dailymealquota end as dfri,
	     case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
             then allshift.dailymealquota end as dsat,*/
		 allshift.dailymealquota,
		 allshift.packagea,
		 allshift.packageb,
		 allshift.dailymealquota,
		 allshift.packagea,
		 allshift.packageb
	     
from(

     select detail.personnum pid,
            CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) weekstartdate,
            'daily' as quotatype,    
	        CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 23) SHIFTSTARTDATE,
	        --,CONVERT(varchar(100), detail.SHIFTENDDATE, 23) SHIFTENDDATE
	        --,detail.mealquota
	        CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, 0, CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 23)) ), 6),121) as expdate,  --??need to generate based on the shift start date
	        CONVERT(nvarchar(10), getdate(),23) lastrundate,
	        sum(detail.shifthours) as shifttotal,
	        case when sum(detail.shifthours) < '4' then 0  --less than 4 hous, no free meal
		         when sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6' then 1   --above or equal to 4 hours,less than 6 hours , 1 free meal
			     when sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12' then 2  --above or equal to 6 hours,less than 12 hours , 2 free meal
			     when sum(detail.shifthours) >= '12'  then 3 --above or equal to 12 hours,  3 free meal
			     else 0 end as dailymealquota 
            ,case  when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '22:00:00' or min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '10:00:00' and CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '22:00:00' ) 
			              then  2*/
					 when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '22:00:00' or min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '02:00:00' ) 
			              then  2
                     when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '02:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '10:00:00' and CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '22:00:00' ) 
			              then  5*/
					 when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '20:00:00' ) 
			              then  1
                     when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '20:00:00' or  min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  2 
					 else 0 end as packagea
             ,case  /*when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '22:00:00' or CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '10:00:00' ) 
			              then  1*/
					 when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '22:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '22:00:00' or CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '02:00:00' ) 
			              then  3*/
                     when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '02:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					 when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '22:00:00' ) 
			              then  2
					 when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '20:00:00' ) 
			              then  2
                     when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '20:00:00' or  min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1 
					 else 0 end as packageb
     from (
         SELECT --[SHIFTASSIGNID]
               --,[EMPLOYEEID]
	           person.personnum
               -- ,[SHIFTID]
	          ,[ENTEREDONDTM]
	          ,[SHIFTSTARTDATE]
	          ,[SHIFTENDDATE]
	          , datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) as shifthours
	          /*, case  when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '4' then 0  --less than 4 hous, no free meal

					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '4'  and datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '6' then 1   --above or equal to 4 hours,less than 6 hours , 1 free meal
					
					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '6'  and datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '12' then 2   --above or equal to 6 hours,less than 12 hours , 2 free meal
					
					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '12'  then 3 --above or equal to 12 hours,  3 free meal
						
					else 0 end as mealquota */      
  FROM [wfcpdb].[dbo].[SHIFTASSIGNMNT]
       join [wfcpdb].[dbo].shiftcode on shiftcode.shiftcodeid = SHIFTASSIGNMNT.shiftcodeid
       join [wfcpdb].[dbo].person on person.personid = shiftassignmnt.employeeid
       -- where shiftcode.shiftcodeid in ('413' , '401', '407','411','404') and shiftcode.paycodeid = '137' and deletedsw <> '1'
  where   
       --[ENTEREDONDTM] = getdate()
       --CONVERT(varchar(100), [ENTEREDONDTM], 23) = CONVERT(varchar(100), getdate(), 23)   --modified on today
       CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
         >= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) --???change it to be the current date if the interface run after 00:00
         -->= CONVERT(nvarchar(10), getdate(),23)
       and  CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
         <= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23) 
       and shiftassignmnt.[DELETEDSW] <> '1'
       and (shiftcode.paycodeid  not in ( '128' , '102' , '138') or shiftcode.paycodeid is null) --?need to add the pay code?
       --group by CONVERT(varchar(100), [SHIFTSTARTDATE], 23)
       --order by shiftstartdate
       ) detail
  group by personnum,  CONVERT(varchar(100), [SHIFTSTARTDATE], 23) 

 -- ***********************************************************************
 --/*  /*  weekly update start */
 union
 select 
      dailymeal.pid
      ,CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) weekstartdate
      ,'weekly' as quotatype
      ,CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) weekstartdate
      --, CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 6),121) as expdate
      , CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, 0, dailymeal.weekstartdate) ), 6),121) as expdate  --??need to generate based on the shift start date
      ,CONVERT(nvarchar(10), getdate(),23) lastrundate
      , sum(dailymeal.shifttotal)
      , sum (dailymeal.dailymealquota)
	  ,sum(dailymeal.packagea) as packagea --2020.05.07
	  ,sum(dailymeal.packageb) as packageb --2020.05.07
 from(
      select detail.personnum pid
             ,CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) weekstartdate
             ,'daily' as quotatype    
	         ,CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 23) SHIFTSTARTDATE
	         --,CONVERT(varchar(100), detail.SHIFTENDDATE, 23) SHIFTENDDATE
	  	     --,detail.mealquota
	         ,CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, 0, CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 23)) ), 6),121) as expdate  --??need to generate based on the shift start date
	         ,CONVERT(nvarchar(10), getdate(),23) lastrundate
	         ,sum(detail.shifthours) as shifttotal
	         ,case  when sum(detail.shifthours) < '4' then 0  --less than 4 hous, no free meal

					when sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6' then 1   --above or equal to 4 hours,less than 6 hours , 1 free meal
					
					when sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12' then 2  --above or equal to 6 hours,less than 12 hours , 2 free meal
					
					when sum(detail.shifthours) >= '12'  then 3 --above or equal to 12 hours,  3 free meal
						
					else 0 end as dailymealquota 
			,case  when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '22:00:00' or min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '10:00:00' and CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '22:00:00' ) 
			              then  2*/
					 when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '22:00:00' or min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '02:00:00' ) 
			              then  2
                     when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '02:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '10:00:00' and CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '22:00:00' ) 
			              then  5*/
					 when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '20:00:00' ) 
			              then  1
                     when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '20:00:00' or  min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  2 
					 else 0 end as packagea
             ,case  /*when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '22:00:00' or CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '10:00:00' ) 
			              then  1*/
					 when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '22:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '22:00:00' or CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '02:00:00' ) 
			              then  3*/
                     when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '02:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					 when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '22:00:00' ) 
			              then  2
					 when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '20:00:00' ) 
			              then  2
                     when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '20:00:00' or  min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1 
					 else 0 end as packageb
			
        from (
             SELECT --[SHIFTASSIGNID]
                    --,[EMPLOYEEID]
	                person.personnum
                    -- ,[SHIFTID]
	                ,[ENTEREDONDTM]
	                ,[SHIFTSTARTDATE]
	                ,[SHIFTENDDATE]
	                ,datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) as shifthours
	                /*, case  when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '4' then 0  --less than 4 hous, no free meal

					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '4'  and datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '6' then 1   --above or equal to 4 hours,less than 6 hours , 1 free meal
					
					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '6'  and datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '12' then 2  --above or equal to 6 hours,less than 12 hours , 2 free meal
					
					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '12'  then 3 --above or equal to 12 hours,  3 free meal
						
					else 0 end as mealquota */      
             FROM [wfcpdb].[dbo].[SHIFTASSIGNMNT]
                  join [wfcpdb].[dbo].shiftcode on shiftcode.shiftcodeid = SHIFTASSIGNMNT.shiftcodeid
                  join [wfcpdb].[dbo].person on person.personid = shiftassignmnt.employeeid
                  -- where shiftcode.shiftcodeid in ('413' , '401', '407','411','404') and shiftcode.paycodeid = '137' and deletedsw <> '1'
             where   
                  --[ENTEREDONDTM] = getdate()
                  --CONVERT(varchar(100), [ENTEREDONDTM], 23) = CONVERT(varchar(100), getdate(), 23)   --modified on today
                  CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
                       >= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) --???change it to be the current date if the interface run after 00:00
                       -->= CONVERT(nvarchar(10), getdate(),23)
                  and  CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
                      <= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23) 
                  and shiftassignmnt.[DELETEDSW] <> '1'
                  and (shiftcode.paycodeid  not in ( '128' , '102' , '138') or shiftcode.paycodeid is null) --?need to add the pay code?
                  --group by CONVERT(varchar(100), [SHIFTSTARTDATE], 23)
                  --order by shiftstartdate
                  ) detail
				  
                 group by personnum,  CONVERT(varchar(100), [SHIFTSTARTDATE], 23)  ) dailymeal
				 
  group by pid, dailymeal.weekstartdate 
  --*/   /*  weekly update end*/
  ) allshift

  where 
       (select count(1) as num 
	    from [wfcpdb].[dbo].ktc_freemealquota  
        where ktc_freemealquota.fld_personnum = allshift.pid 
		      and  ktc_freemealquota.fld_weekstartdate = allshift.weekstartdate
              and ktc_freemealquota.fld_quotatype = allshift.quotatype 
			  and ktc_freemealquota.fld_ddate = allshift.SHIFTSTARTDATE ) = 0
		and allshift.shiftstartdate >= CONVERT(nvarchar(10), getdate(),23) -- 20200508 only update the data from today
 --initial quota creation end	

 ----------------------------------------------------------------------------------------------------------------------
 --clear the quota for the schedule cancelation  Start


update [wfcpdb].[dbo].ktc_freemealquota
        set fld_personnum = deactshift.fld_personnum, 
            fld_quotatype= deactshift.fld_quotatype, 
            fld_ddate = deactshift.fld_ddate, 
            fld_expdate = deactshift.fld_expdate, 
            fld_shiftlength = 0, 
            fld_lastrunresult = 0, 
			fld_lastrunresulta = 0,
			fld_lastrunresultb = 0,
			/*fld_lastrunresult = case when deactshift.fld_ddate >= CONVERT(nvarchar(10), getdate(),23) then 0 end, 
			fld_lastrunresulta = case when deactshift.fld_ddate >= CONVERT(nvarchar(10), getdate(),23) then 0 end,
			fld_lastrunresultb = case when deactshift.fld_ddate >= CONVERT(nvarchar(10), getdate(),23) then 0 end,*/-- 20200508 only update the data from today
            fld_lastrundate =  CONVERT(nvarchar(10), getdate(),23), 
            fld_weekstartdate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23),
            fld_delta = 0 -  (
                 case when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                          then ktc_freemealquota.fld_dsun
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
                          then ktc_freemealquota.fld_dmon
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
                          then ktc_freemealquota.fld_dtue
                      when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
                          then ktc_freemealquota.fld_dwed
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
                          then ktc_freemealquota.fld_dtur
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
                          then ktc_freemealquota.fld_dfri
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
                          then ktc_freemealquota.fld_dsat
	                  else 0  end ),
			fld_deltaa = 0 -  (
                 case when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                          then ktc_freemealquota.fld_dsuna
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
                          then ktc_freemealquota.fld_dmona
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
                          then ktc_freemealquota.fld_dtuea
                      when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
                          then ktc_freemealquota.fld_dweda
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
                          then ktc_freemealquota.fld_dtura
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
                          then ktc_freemealquota.fld_dfria
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
                          then ktc_freemealquota.fld_dsata
	                  else 0  end ),
			fld_deltab = 0 -  (
                 case when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                          then ktc_freemealquota.fld_dsunb
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
                          then ktc_freemealquota.fld_dmonb
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
                          then ktc_freemealquota.fld_dtueb
                      when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
                          then ktc_freemealquota.fld_dwedb
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
                          then ktc_freemealquota.fld_dturb
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
                          then ktc_freemealquota.fld_dfrib
	                  when ktc_freemealquota.fld_lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
                          then ktc_freemealquota.fld_dsatb
	                  else 0  end )
			/* fld_dsun = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
                              then 0 end ),
	         fld_dmon = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
                              then 0 end ),
			 fld_dtue = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
                              then 0 end ),
			 fld_dwed = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
                              then 0 end ),
	         fld_dtur = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
                              then 0 end ),
			 fld_dfri = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
                              then 0 end ),
			 fld_dsat = (case when CONVERT(nvarchar(10), getdate(),23) = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
                              then 0 end )*/

from (
--get the shift be removed from the schedule
-------------------------------------------------------------------------
 select * 
 from [wfcpdb].[dbo].ktc_freemealquota 
 where	(select count(1) as num from(

   select
	     allshift.pid,
         allshift.weekstartdate,
	     allshift.quotatype,
	     allshift.SHIFTSTARTDATE,
	     allshift.expdate,
	     allshift.lastrundate,
	     allshift.shifttotal,
	     allshift.dailymealquota,
	     case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23)
             then allshift.dailymealquota end as dsun, 
	     case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 0),23)
             then allshift.dailymealquota end as dmon,
	     case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 1),23)
             then allshift.dailymealquota end as dtue,
         case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 2),23)
             then allshift.dailymealquota end as dwed,
	     case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 3),23)
             then allshift.dailymealquota end as dtur,
	     case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 4),23)
             then allshift.dailymealquota end as dfri,
	     case when allshift.lastrundate = CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23)
             then allshift.dailymealquota end as dsat
	     
    from(

     select detail.personnum pid,
            CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) weekstartdate,
            'daily' as quotatype,    
	        CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 23) SHIFTSTARTDATE,
	        --,CONVERT(varchar(100), detail.SHIFTENDDATE, 23) SHIFTENDDATE
	        --,detail.mealquota
	        CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, 0, CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 23)) ), 6),121) as expdate,  --??need to generate based on the shift start date
	        CONVERT(nvarchar(10), getdate(),23) lastrundate,
	        sum(detail.shifthours) as shifttotal,
	        case when sum(detail.shifthours) < '4' then 0  --less than 4 hous, no free meal
		         when sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6' then 1   --above or equal to 4 hours,less than 6 hours , 1 free meal
			     when sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12' then 2  --above or equal to 6 hours,less than 12 hours , 2 free meal
			     when sum(detail.shifthours) >= '12'  then 3 --above or equal to 12 hours,  3 free meal
			     else 0 end as dailymealquota 
			,case  when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '22:00:00' or min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '10:00:00' and CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '22:00:00' ) 
			              then  2*/
					 when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '22:00:00' or min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '02:00:00' ) 
			              then  2
                     when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '02:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '10:00:00' and CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '22:00:00' ) 
			              then  5*/
					 when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '20:00:00' ) 
			              then  1
                     when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '20:00:00' or  min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  2 
					 else 0 end as packagea
             ,case  /*when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '22:00:00' or CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '10:00:00' ) 
			              then  1*/
					 when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '22:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '22:00:00' or CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '02:00:00' ) 
			              then  3*/
                     when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '02:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					 when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '22:00:00' ) 
			              then  2
					 when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '20:00:00' ) 
			              then  2
                     when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '20:00:00' or  min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1 
					 else 0 end as packageb
     from (
         SELECT --[SHIFTASSIGNID]
               --,[EMPLOYEEID]
	           person.personnum
               -- ,[SHIFTID]
	          ,[ENTEREDONDTM]
	          ,[SHIFTSTARTDATE]
	          ,[SHIFTENDDATE]
	          , datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) as shifthours
	          /*, case  when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '4' then 0  --less than 4 hous, no free meal

					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '4'  and datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '6' then 1   --above or equal to 4 hours,less than 6 hours , 1 free meal
					
					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '6'  and datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '12' then 2   --above or equal to 6 hours,less than 12 hours , 2 free meal
					
					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '12'  then 3 --above or equal to 12 hours,  3 free meal
						
					else 0 end as mealquota */      
  FROM [wfcpdb].[dbo].[SHIFTASSIGNMNT]
       join [wfcpdb].[dbo].shiftcode on shiftcode.shiftcodeid = SHIFTASSIGNMNT.shiftcodeid
       join [wfcpdb].[dbo].person on person.personid = shiftassignmnt.employeeid
       -- where shiftcode.shiftcodeid in ('413' , '401', '407','411','404') and shiftcode.paycodeid = '137' and deletedsw <> '1'
  where   
       --[ENTEREDONDTM] = getdate()
       --CONVERT(varchar(100), [ENTEREDONDTM], 23) = CONVERT(varchar(100), getdate(), 23)   --modified on today
       CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
          >= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) --???change it to be the current date if the interface run after 00:00
         -->= CONVERT(nvarchar(10), getdate(),23)
       and  CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
         <= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23) 
       and shiftassignmnt.[DELETEDSW] <> '1'
       and (shiftcode.paycodeid  not in ( '128' , '102' , '138') or shiftcode.paycodeid is null) --?need to add the pay code?
       --group by CONVERT(varchar(100), [SHIFTSTARTDATE], 23)
       --order by shiftstartdate
       ) detail
  group by personnum,  CONVERT(varchar(100), [SHIFTSTARTDATE], 23) 

 -- ***********************************************************************
 --/*
 
 union
 select 
      dailymeal.pid
      ,CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) weekstartdate
      ,'weekly' as quotatype
      ,CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) weekstartdate
      --, CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 6),121) as expdate
      , CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, 0, dailymeal.weekstartdate) ), 6),121) as expdate  --??need to generate based on the shift start date
      ,CONVERT(nvarchar(10), getdate(),23) lastrundate
      , sum(dailymeal.shifttotal)
      , sum (dailymeal.dailymealquota)
	  ,sum(dailymeal.packagea) as packagea --2020.05.07
	  ,sum(dailymeal.packageb) as packageb --2020.05.07
 from(
      select detail.personnum pid
             ,CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) weekstartdate
             ,'daily' as quotatype    
	         ,CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 23) SHIFTSTARTDATE
	         --,CONVERT(varchar(100), detail.SHIFTENDDATE, 23) SHIFTENDDATE
	  	     --,detail.mealquota
	         ,CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, 0, CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 23)) ), 6),121) as expdate  --??need to generate based on the shift start date
	         ,CONVERT(nvarchar(10), getdate(),23) lastrundate
	         ,sum(detail.shifthours) as shifttotal
	         ,case  when sum(detail.shifthours) < '4' then 0  --less than 4 hous, no free meal

					when sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6' then 1   --above or equal to 4 hours,less than 6 hours , 1 free meal
					
					when sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12' then 2  --above or equal to 6 hours,less than 12 hours , 2 free meal
					
					when sum(detail.shifthours) >= '12'  then 3 --above or equal to 12 hours,  3 free meal
						
					else 0 end as dailymealquota 
			,case  when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '22:00:00' or min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '10:00:00' and CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '22:00:00' ) 
			              then  2*/
					 when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '22:00:00' or min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '02:00:00' ) 
			              then  2
                     when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '02:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '10:00:00' and CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '22:00:00' ) 
			              then  5*/
					 when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '20:00:00' ) 
			              then  1
                     when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '20:00:00' or  min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  2 
					 else 0 end as packagea
             ,case  /*when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '22:00:00' or CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '10:00:00' ) 
			              then  1*/
					 when (sum(detail.shifthours) >= '4'  and sum(detail.shifthours) < '6') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '22:00:00' ) 
			              then  1
					/* when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) >= '22:00:00' or CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24) < '02:00:00' ) 
			              then  3*/
                     when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '02:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1
					 when (sum(detail.shifthours) >= '6'  and sum(detail.shifthours) < '12') and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '22:00:00' ) 
			              then  2
					 when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '10:00:00' and min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '20:00:00' ) 
			              then  2
                     when sum(detail.shifthours) >= '12'  and (min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) >= '20:00:00' or  min(CONVERT(varchar(100), detail.[SHIFTSTARTDATE], 24)) < '10:00:00' ) 
			              then  1 
					 else 0 end as packageb
        from (
             SELECT --[SHIFTASSIGNID]
                    --,[EMPLOYEEID]
	                person.personnum
                    -- ,[SHIFTID]
	                ,[ENTEREDONDTM]
	                ,[SHIFTSTARTDATE]
	                ,[SHIFTENDDATE]
	                ,datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) as shifthours
	                /*, case  when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '4' then 0  --less than 4 hous, no free meal

					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '4'  and datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '6' then 1   --above or equal to 4 hours,less than 6 hours , 1 free meal
					
					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '6'  and datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) < '12' then 2  --above or equal to 6 hours,less than 12 hours , 2 free meal
					
					when datediff(hour,SHIFTSTARTDATE,SHIFTENDDATE) >= '12'  then 3 --above or equal to 12 hours,  3 free meal
						
					else 0 end as mealquota */      
             FROM [wfcpdb].[dbo].[SHIFTASSIGNMNT]
                  join [wfcpdb].[dbo].shiftcode on shiftcode.shiftcodeid = SHIFTASSIGNMNT.shiftcodeid
                  join [wfcpdb].[dbo].person on person.personid = shiftassignmnt.employeeid
                  -- where shiftcode.shiftcodeid in ('413' , '401', '407','411','404') and shiftcode.paycodeid = '137' and deletedsw <> '1'
             where   
                  --[ENTEREDONDTM] = getdate()
                  --CONVERT(varchar(100), [ENTEREDONDTM], 23) = CONVERT(varchar(100), getdate(), 23)   --modified on today
                  CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
                       >= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), -1),23) --???change it to be the current date if the interface run after 00:00
                       -->= CONVERT(nvarchar(10), getdate(),23)
                  and  CONVERT(varchar(100), [wfcpdb].[dbo].[SHIFTASSIGNMNT].SHIFTSTARTDATE, 23) 
                       <= CONVERT(nvarchar(10), DATEADD(wk, DATEDIFF(wk,0,DATEADD(dd, -1, getdate()) ), 5),23) 
                  and shiftassignmnt.[DELETEDSW] <> '1'
                  and (shiftcode.paycodeid  not in ( '128' , '102' , '138') or shiftcode.paycodeid is null) --?need to add the pay code?
                  --group by CONVERT(varchar(100), [SHIFTSTARTDATE], 23)
                  --order by shiftstartdate
                  ) detail
                 group by personnum,  CONVERT(varchar(100), [SHIFTSTARTDATE], 23)  ) dailymeal

  group by pid, dailymeal.weekstartdate 
  --*/  /* weekly update end*/
  ) allshift ) allshift1
  where      allshift1.pid  =  ktc_freemealquota.fld_personnum  
		      and allshift1.weekstartdate = ktc_freemealquota.fld_weekstartdate  
              and allshift1.quotatype = ktc_freemealquota.fld_quotatype  
			  and allshift1.SHIFTSTARTDATE = ktc_freemealquota.fld_ddate )  =  0 ) deactshift

where  [ktc_freemealquota].fld_personnum = deactshift.fld_personnum 
and  [ktc_freemealquota].fld_quotatype= deactshift.fld_quotatype 
and [ktc_freemealquota].fld_ddate = deactshift.fld_ddate  
and [ktc_freemealquota].fld_expdate = deactshift.fld_expdate
and [ktc_freemealquota].fld_ddate >= CONVERT(nvarchar(10), getdate(),23) -- 20200508 only update the data from today 

 --clear the quota for the schedule cancelation  End
 ---------------------------------------------------------------------------------


 --output test
 SELECT [fld_personnum]
      ,[fld_weekstartdate]
      ,[fld_quotatype]
      ,[fld_ddate]
      ,[fld_expdate]
      ,[fld_lastrundate]
      ,[fld_shiftlength]
	  ,[fld_lastrunresulta]
      ,[fld_lastrunresultb]
   -- ,[fld_lastrunresult]
      ,[fld_deltaa]
      ,[fld_deltab]
      ,[fld_delta] 
      ,[fld_dsuna]
      ,[fld_dsunb]
      ,[fld_dsun]
      ,[fld_dmona]
      ,[fld_dmonb]
      ,[fld_dmon]
      ,[fld_dtuea]
      ,[fld_dtueb]
      ,[fld_dtue]
      ,[fld_dweda]
      ,[fld_dwedb]
      ,[fld_dwed]
      ,[fld_dtura]
      ,[fld_dturb]
      ,[fld_dtur]
      ,[fld_dfria]
      ,[fld_dfrib]
      ,[fld_dfri]
      ,[fld_dsata]
      ,[fld_dsatb]
      ,[fld_dsat] 
  
	  FROM [wfcpdb].[dbo].[ktc_freemealquota] 
  where 
  --fld_expdate = '2020-05-03'
  fld_personnum = '30000159'
  order by fld_personnum, fld_ddate , fld_quotatype
