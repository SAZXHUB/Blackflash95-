local v0=string.char;local v1=string.byte;local v2=string.sub;local v3=bit32 or bit ;local v4=v3.bxor;local v5=table.concat;local v6=table.insert;local function v7(v24,v25) local v26={};for v41=1, #v24 do v6(v26,v0(v4(v1(v2(v24,v41,v41 + 1 )),v1(v2(v25,1 + (v41% #v25) ,1 + (v41% #v25) + 1 )))%256 ));end return v5(v26);end local v8=tonumber;local v9=string.byte;local v10=string.char;local v11=string.sub;local v12=string.gsub;local v13=string.rep;local v14=table.concat;local v15=table.insert;local v16=math.ldexp;local v17=getfenv or function() return _ENV;end ;local v18=setmetatable;local v19=pcall;local v20=select;local v21=unpack or table.unpack ;local v22=tonumber;local function v23(v27,v28,...) local v29=1;local v30;v27=v12(v11(v27,5),v7("\19\184","\164\61\150\74\227\222"),function(v42) if (v9(v42,2)==(246 -167)) then local v90=0;while true do if (v90==0) then v30=v8(v11(v42,1,1));return "";end end else local v91=v10(v8(v42,16));if v30 then local v98=0;local v99;while true do if (v98==0) then v99=v13(v91,v30);v30=nil;v98=1;end if (v98==1) then return v99;end end else return v91;end end end);local function v31(v43,v44,v45) if v45 then local v92=(v43/(2^(v44-1)))%((5 -3)^(((v45-1) -(v44-1)) + 1)) ;return v92-(v92%1) ;else local v93=0;local v94;while true do if (v93==0) then v94=2^(v44-1) ;return (((v43%(v94 + v94))>=v94) and 1) or 0 ;end end end end local function v32() local v46=0;local v47;while true do if (v46==0) then v47=v9(v27,v29,v29);v29=v29 + (1 -0) ;v46=1;end if (1==v46) then return v47;end end end local function v33() local v48=0;local v49;local v50;while true do if (v48==0) then v49,v50=v9(v27,v29,v29 + 2 );v29=v29 + 2 ;v48=1;end if (v48==1) then return (v50 * 256) + v49 ;end end end local function v34() local v51=0;local v52;local v53;local v54;local v55;while true do if (v51==0) then v52,v53,v54,v55=v9(v27,v29,v29 + 3 );v29=v29 + 4 ;v51=1;end if (v51==1) then return (v55 * 16777216) + (v54 * 65536) + (v53 * 256) + v52 ;end end end local function v35() local v56=0;local v57;local v58;local v59;local v60;local v61;local v62;while true do if (v56==0) then v57=v34();v58=v34();v56=1;end if (v56==2) then v61=v31(v58,21,31);v62=((v31(v58,32)==1) and  -1) or 1 ;v56=3;end if (1==v56) then v59=1;v60=(v31(v58,1,20) * ((4 -2)^32)) + v57 ;v56=2;end if (v56==3) then if (v61==0) then if (v60==0) then return v62 * 0 ;else local v123=0;while true do if (v123==0) then v61=1;v59=0;break;end end end elseif (v61==2047) then return ((v60==0) and (v62 * ((620 -(555 + 64))/(931 -(857 + 74))))) or (v62 * NaN) ;end return v16(v62,v61-1023 ) * (v59 + (v60/(2^52))) ;end end end local function v36(v63) local v64=0;local v65;local v66;while true do if (v64==3) then return v14(v66);end if (0==v64) then v65=nil;if  not v63 then local v116=0;while true do if (v116==0) then v63=v34();if (v63==0) then return "";end break;end end end v64=1;end if (v64==2) then v66={};for v100=1, #v65 do v66[v100]=v10(v9(v11(v65,v100,v100)));end v64=3;end if (v64==1) then v65=v11(v27,v29,(v29 + v63) -1 );v29=v29 + v63 ;v64=2;end end end local v37=v34;local function v38(...) return {...},v20("#",...);end local function v39() local v67={};local v68={};local v69={};local v70={v67,v68,nil,v69};local v71=v34();local v72={};for v81=928 -(214 + 713) ,v71 do local v82=v32();local v83;if (v82==1) then v83=v32()~=(0 + 0) ;elseif (v82==2) then v83=v35();elseif (v82==3) then v83=v36();end v72[v81]=v83;end v70[3]=v32();for v85=1 + 0 ,v34() do local v86=0;local v87;while true do if (0==v86) then v87=v32();if (v31(v87,1,878 -(282 + 595) )==0) then local v119=0;local v120;local v121;local v122;while true do if (v119==1) then v122={v33(),v33(),nil,nil};if (v120==0) then local v131=0;while true do if (v131==0) then v122[3]=v33();v122[4]=v33();break;end end elseif (v120==1) then v122[3]=v34();elseif (v120==2) then v122[3]=v34() -(2^16) ;elseif (v120==3) then local v142=0;while true do if (v142==0) then v122[3]=v34() -(2^16) ;v122[4]=v33();break;end end end v119=2;end if (v119==3) then if (v31(v121,3,3)==1) then v122[1641 -(1523 + 114) ]=v72[v122[4]];end v67[v85]=v122;break;end if (v119==2) then if (v31(v121,1,1)==1) then v122[2]=v72[v122[2]];end if (v31(v121,2,2)==1) then v122[3]=v72[v122[3]];end v119=3;end if (v119==0) then v120=v31(v87,2,3);v121=v31(v87,4,6);v119=1;end end end break;end end end for v88=1,v34() do v68[v88-1 ]=v39();end return v70;end local function v40(v74,v75,v76) local v77=0;local v78;local v79;local v80;while true do if (1==v77) then v80=v74[3];return function(...) local v102=v78;local v103=v79;local v104=v80;local v105=v38;local v106=1;local v107= -1;local v108={};local v109={...};local v110=v20("#",...) -1 ;local v111={};local v112={};for v117=0,v110 do if (v117>=v104) then v108[v117-v104 ]=v109[v117 + 1 + 0 ];else v112[v117]=v109[v117 + (1 -0) ];end end local v113=(v110-v104) + 1 ;local v114;local v115;while true do local v118=0;while true do if (v118==0) then v114=v102[v106];v115=v114[1];v118=1;end if (v118==1) then if (v115<=39) then if (v115<=19) then if (v115<=9) then if (v115<=4) then if (v115<=1) then if (v115>(1065 -(68 + 997))) then do return v112[v114[2]]();end elseif v112[v114[2]] then v106=v106 + (1271 -(226 + 1044)) ;else v106=v114[3];end elseif (v115<=2) then if (v114[2]==v112[v114[4]]) then v106=v106 + 1 ;else v106=v114[3];end elseif (v115>3) then v112[v114[2]]=v75[v114[3]];else for v305=v114[2],v114[3] do v112[v305]=nil;end end elseif (v115<=6) then if (v115>5) then v76[v114[3]]=v112[v114[2]];else v112[v114[2]]=v112[v114[3]][v114[4]];end elseif (v115<=7) then if  not v112[v114[2]] then v106=v106 + 1 ;else v106=v114[3];end elseif (v115==8) then local v244=0;local v245;while true do if (0==v244) then v245=v114[2];v112[v245]=v112[v245](v21(v112,v245 + 1 ,v114[3]));break;end end else v106=v114[3];end elseif (v115<=14) then if (v115<=11) then if (v115==10) then local v149=0;local v150;local v151;local v152;while true do if (v149==1) then v152={};v151=v18({},{[v7("\122\16\240\61\86\6\93","\99\37\79\153\83\50")]=function(v338,v339) local v340=0;local v341;while true do if (0==v340) then v341=v152[v339];return v341[4 -3 ][v341[2]];end end end,[v7("\228\114\83\243\204\68\83\242\222\85","\150\187\45\61")]=function(v342,v343,v344) local v345=0;local v346;while true do if (v345==0) then v346=v152[v343];v346[1][v346[2]]=v344;break;end end end});v149=2;end if (v149==0) then v150=v103[v114[3]];v151=nil;v149=1;end if (v149==2) then for v347=1,v114[4] do v106=v106 + 1 ;local v348=v102[v106];if (v348[1]==40) then v152[v347-1 ]={v112,v348[120 -(32 + 85) ]};else v152[v347-1 ]={v75,v348[3]};end v111[ #v111 + 1 ]=v152;end v112[v114[2]]=v40(v150,v151,v76);break;end end else local v153=0;local v154;local v155;while true do if (v153==0) then v154=v114[2];v155=v112[v154];v153=1;end if (v153==1) then for v350=v154 + 1 + 0 ,v107 do v15(v155,v112[v350]);end break;end end end elseif (v115<=12) then v112[v114[1 + 1 ]]=v112[v114[3]] + v114[4] ;elseif (v115>13) then v112[v114[2]]=v75[v114[3]];else v112[v114[2]]= #v112[v114[960 -(892 + 65) ]];end elseif (v115<=16) then if (v115==(35 -20)) then v112[v114[2]]=v112[v114[3]]%v112[v114[6 -2 ]] ;else v112[v114[2]]=v112[v114[3]]%v114[4] ;end elseif (v115<=17) then v76[v114[4 -1 ]]=v112[v114[2]];elseif (v115==18) then v112[v114[2]]=v76[v114[3]];else do return;end end elseif (v115<=29) then if (v115<=24) then if (v115<=21) then if (v115>20) then local v161=0;local v162;local v163;while true do if (1==v161) then for v351=1, #v111 do local v352=0;local v353;while true do if (v352==0) then v353=v111[v351];for v433=0, #v353 do local v434=0;local v435;local v436;local v437;while true do if (v434==0) then v435=v353[v433];v436=v435[1];v434=1;end if (v434==1) then v437=v435[2];if ((v436==v112) and (v437>=v162)) then local v461=0;while true do if (v461==0) then v163[v437]=v436[v437];v435[1]=v163;break;end end end break;end end end break;end end end break;end if (v161==0) then v162=v114[2];v163={};v161=1;end end else local v164=0;local v165;local v166;local v167;while true do if (v164==0) then v165=v114[2];v166=v112[v165];v164=1;end if (1==v164) then v167=v112[v165 + 2 ];if (v167>(350 -(87 + 263))) then if (v166>v112[v165 + 1 ]) then v106=v114[3];else v112[v165 + 3 ]=v166;end elseif (v166<v112[v165 + 1 ]) then v106=v114[3];else v112[v165 + 3 ]=v166;end break;end end end elseif (v115<=22) then if  not v112[v114[2]] then v106=v106 + 1 ;else v106=v114[3];end elseif (v115>23) then v112[v114[2]]=v112[v114[3]]%v114[4] ;else local v254=0;local v255;local v256;local v257;while true do if (0==v254) then v255=v114[2];v256={v112[v255](v112[v255 + 1 ])};v254=1;end if (v254==1) then v257=0;for v398=v255,v114[4] do v257=v257 + 1 ;v112[v398]=v256[v257];end break;end end end elseif (v115<=(206 -(67 + 113))) then if (v115>(19 + 6)) then v112[v114[2]][v114[3]]=v112[v114[4]];else local v170=v114[2];v112[v170](v21(v112,v170 + (2 -1) ,v114[3]));end elseif (v115<=27) then v112[v114[2]]= #v112[v114[3]];elseif (v115>(21 + 7)) then local v258=v114[2];local v259,v260=v105(v112[v258](v21(v112,v258 + (3 -2) ,v107)));v107=(v260 + v258) -1 ;local v261=0;for v315=v258,v107 do local v316=0;while true do if (v316==0) then v261=v261 + 1 ;v112[v315]=v259[v261];break;end end end else v112[v114[2]]=v114[3];end elseif (v115<=(986 -(802 + 150))) then if (v115<=31) then if (v115==30) then local v172=0;local v173;local v174;local v175;while true do if (v172==2) then for v354=1,v114[4] do local v355=0;local v356;while true do if (v355==0) then v106=v106 + (1 -0) ;v356=v102[v106];v355=1;end if (v355==1) then if (v356[1 + 0 ]==40) then v175[v354-1 ]={v112,v356[3]};else v175[v354-1 ]={v75,v356[3]};end v111[ #v111 + 1 ]=v175;break;end end end v112[v114[2]]=v40(v173,v174,v76);break;end if (v172==0) then v173=v103[v114[3]];v174=nil;v172=1;end if (v172==1) then v175={};v174=v18({},{[v7("\35\76\162\125\24\118\179","\19\124\19\203")]=function(v357,v358) local v359=v175[v358];return v359[2 -1 ][v359[2]];end,[v7("\254\45\3\240\21\121\183\197\23\21","\217\161\114\109\149\98\16")]=function(v360,v361,v362) local v363=0;local v364;while true do if (v363==0) then v364=v175[v361];v364[1][v364[2]]=v362;break;end end end});v172=2;end end else local v176=0;local v177;local v178;local v179;while true do if (v176==0) then v177=v114[2];v178={v112[v177](v112[v177 + 1 ])};v176=1;end if (v176==1) then v179=0;for v365=v177,v114[4] do local v366=0;while true do if (v366==0) then v179=v179 + 1 ;v112[v365]=v178[v179];break;end end end break;end end end elseif (v115<=32) then v112[v114[2]]=v114[3] + v112[v114[4]] ;elseif (v115==33) then v112[v114[2]]={};else v112[v114[2]][v114[3]]=v114[4];end elseif (v115<=36) then if (v115>35) then if (v112[v114[2]]==v114[4]) then v106=v106 + 1 ;else v106=v114[3];end else local v181=0;local v182;while true do if (v181==0) then v182=v114[2];v112[v182]=v112[v182](v21(v112,v182 + 1 ,v107));break;end end end elseif (v115<=37) then do return;end elseif (v115==38) then v106=v114[8 -5 ];else v112[v114[2]]=v76[v114[3]];end elseif (v115<=59) then if (v115<=49) then if (v115<=(26 + 18)) then if (v115<=41) then if (v115>40) then local v183=0;local v184;while true do if (0==v183) then v184=v114[2];v112[v184]=v112[v184](v21(v112,v184 + 1 ,v114[3]));break;end end else v112[v114[2]]=v112[v114[3]];end elseif (v115<=42) then local v187=0;local v188;while true do if (v187==0) then v188=v114[2];v112[v188](v21(v112,v188 + 1 ,v107));break;end end elseif (v115==43) then local v271=0;local v272;local v273;while true do if (v271==0) then v272=v114[2];v273=v112[v114[3]];v271=1;end if (v271==1) then v112[v272 + 1 ]=v273;v112[v272]=v273[v114[4]];break;end end else local v274=0;local v275;while true do if (v274==0) then v275=v114[2];do return v21(v112,v275,v107);end break;end end end elseif (v115<=46) then if (v115==45) then local v189=0;local v190;local v191;local v192;local v193;while true do if (v189==1) then v107=(v192 + v190) -1 ;v193=0;v189=2;end if (2==v189) then for v367=v190,v107 do local v368=0;while true do if (v368==0) then v193=v193 + 1 ;v112[v367]=v191[v193];break;end end end break;end if (v189==0) then v190=v114[2];v191,v192=v105(v112[v190](v112[v190 + 1 ]));v189=1;end end else v112[v114[2]]=v112[v114[3]];end elseif (v115<=47) then local v196=0;local v197;local v198;local v199;local v200;while true do if (2==v196) then for v369=v197,v107 do local v370=0;while true do if (0==v370) then v200=v200 + 1 ;v112[v369]=v198[v200];break;end end end break;end if (1==v196) then v107=(v199 + v197) -1 ;v200=0;v196=2;end if (v196==0) then v197=v114[2];v198,v199=v105(v112[v197](v21(v112,v197 + (1 -0) ,v114[1190 -(1069 + 118) ])));v196=1;end end elseif (v115>(108 -60)) then local v276=0;local v277;while true do if (v276==0) then v277=v114[2];v112[v277](v21(v112,v277 + 1 ,v107));break;end end else v112[v114[2]][v114[3]]=v112[v114[4]];end elseif (v115<=54) then if (v115<=51) then if (v115==50) then local v201=v114[2];v112[v201](v112[v201 + 1 ]);else for v237=v114[2],v114[3] do v112[v237]=nil;end end elseif (v115<=52) then v112[v114[3 -1 ]]=v112[v114[3]][v114[4]];elseif (v115>53) then v112[v114[2]]=v114[1 + 2 ];else do return v112[v114[2]]();end end elseif (v115<=56) then if (v115>55) then local v204=v114[2];local v205=v112[v114[3]];v112[v204 + 1 ]=v205;v112[v204]=v205[v114[4]];else local v209=0;local v210;local v211;local v212;while true do if (v209==1) then v212=v112[v210] + v211 ;v112[v210]=v212;v209=2;end if (v209==0) then v210=v114[2];v211=v112[v210 + 2 ];v209=1;end if (v209==2) then if (v211>0) then if (v212<=v112[v210 + 1 ]) then v106=v114[3];v112[v210 + 3 ]=v212;end elseif (v212>=v112[v210 + 1 ]) then local v427=0;while true do if (v427==0) then v106=v114[3];v112[v210 + 3 ]=v212;break;end end end break;end end end elseif (v115<=57) then v112[v114[2]]=v112[v114[3]] + v114[4] ;elseif (v115>58) then v112[v114[2]]=v112[v114[3]]%v112[v114[4]] ;elseif (v114[2]==v112[v114[6 -2 ]]) then v106=v106 + 1 ;else v106=v114[3];end elseif (v115<=(69 + 0)) then if (v115<=64) then if (v115<=61) then if (v115>60) then v112[v114[2]]();else local v214=0;local v215;while true do if (v214==0) then v215=v114[793 -(368 + 423) ];do return v112[v215](v21(v112,v215 + (3 -2) ,v114[3]));end break;end end end elseif (v115<=(80 -(10 + 8))) then local v216=0;local v217;local v218;while true do if (0==v216) then v217=v114[2];v218={};v216=1;end if (v216==1) then for v372=1, #v111 do local v373=0;local v374;while true do if (v373==0) then v374=v111[v372];for v438=0, #v374 do local v439=0;local v440;local v441;local v442;while true do if (v439==1) then v442=v440[2];if ((v441==v112) and (v442>=v217)) then v218[v442]=v441[v442];v440[1]=v218;end break;end if (v439==0) then v440=v374[v438];v441=v440[1];v439=1;end end end break;end end end break;end end elseif (v115>63) then v112[v114[2]]=v114[3] + v112[v114[4]] ;else local v284=v114[2];do return v21(v112,v284,v107);end end elseif (v115<=66) then if (v115==65) then v112[v114[2]]();elseif v112[v114[7 -5 ]] then v106=v106 + 1 ;else v106=v114[3];end elseif (v115<=67) then v112[v114[2]][v114[445 -(416 + 26) ]]=v114[4];elseif (v115==68) then local v286=v114[2];local v287=v112[v286 + 2 ];local v288=v112[v286] + v287 ;v112[v286]=v288;if (v287>0) then if (v288<=v112[v286 + 1 ]) then local v403=0;while true do if (v403==0) then v106=v114[3];v112[v286 + 3 ]=v288;break;end end end elseif (v288>=v112[v286 + 1 ]) then local v404=0;while true do if (v404==0) then v106=v114[3];v112[v286 + 3 ]=v288;break;end end end else local v290=0;local v291;while true do if (v290==0) then v291=v114[6 -4 ];v112[v291](v112[v291 + 1 ]);break;end end end elseif (v115<=74) then if (v115<=71) then if (v115==70) then local v221=v114[2];v112[v221]=v112[v221](v21(v112,v221 + 1 ,v107));elseif (v112[v114[2]]==v114[2 + 2 ]) then v106=v106 + 1 ;else v106=v114[3];end elseif (v115<=72) then local v223=0;local v224;local v225;local v226;local v227;while true do if (v223==1) then v107=(v226 + v224) -1 ;v227=0;v223=2;end if (2==v223) then for v375=v224,v107 do local v376=0;while true do if (v376==0) then v227=v227 + (1 -0) ;v112[v375]=v225[v227];break;end end end break;end if (v223==0) then v224=v114[2];v225,v226=v105(v112[v224](v21(v112,v224 + 1 ,v114[3])));v223=1;end end elseif (v115>73) then local v293=0;local v294;while true do if (v293==0) then v294=v114[2];v112[v294](v21(v112,v294 + 1 ,v114[3]));break;end end else local v295=v114[2];local v296,v297=v105(v112[v295](v21(v112,v295 + 1 ,v107)));v107=(v297 + v295) -1 ;local v298=0;for v333=v295,v107 do local v334=0;while true do if (v334==0) then v298=v298 + 1 ;v112[v333]=v296[v298];break;end end end end elseif (v115<=76) then if (v115>(513 -(145 + 293))) then local v228=0;local v229;local v230;local v231;local v232;while true do if (2==v228) then for v377=v229,v107 do local v378=0;while true do if (v378==0) then v232=v232 + 1 ;v112[v377]=v230[v232];break;end end end break;end if (v228==1) then v107=(v231 + v229) -1 ;v232=0;v228=2;end if (v228==0) then v229=v114[2];v230,v231=v105(v112[v229](v112[v229 + 1 ]));v228=1;end end else local v233=0;local v234;local v235;while true do if (0==v233) then v234=v114[432 -(44 + 386) ];v235=v112[v234];v233=1;end if (1==v233) then for v379=v234 + (1487 -(998 + 488)) ,v107 do v15(v235,v112[v379]);end break;end end end elseif (v115<=77) then v112[v114[2]]={};elseif (v115>78) then local v299=0;local v300;local v301;local v302;while true do if (v299==1) then v302=v112[v300 + 2 ];if (v302>0) then if (v301>v112[v300 + 1 + 0 ]) then v106=v114[3];else v112[v300 + 3 ]=v301;end elseif (v301<v112[v300 + 1 ]) then v106=v114[3];else v112[v300 + 3 ]=v301;end break;end if (0==v299) then v300=v114[1 + 1 ];v301=v112[v300];v299=1;end end else local v303=0;local v304;while true do if (v303==0) then v304=v114[2];do return v112[v304](v21(v112,v304 + 1 ,v114[3]));end break;end end end v106=v106 + 1 ;break;end end end end;end if (v77==0) then v78=v74[1];v79=v74[2];v77=1;end end end return v40(v39(),{},v28)(...);end return v23("LOL!0D3O0003063O00737472696E6703043O006368617203043O00627974652O033O0073756203053O0062697433322O033O0062697403043O0062786F7203053O007461626C6503063O00636F6E63617403063O00696E7365727403053O006D6174636803083O00746F6E756D62657203053O007063612O6C00243O0012273O00013O0020345O0002001227000100013O002034000100010003001227000200013O002034000200020004001227000300053O0006070003000A000100010004093O000A0001001227000300063O002034000400030007001227000500083O002034000500050009001227000600083O00203400060006000A00060A00073O000100062O00283O00064O00288O00283O00044O00283O00014O00283O00024O00283O00053O001227000800013O00203400080008000B0012270009000C3O001227000A000D3O00060A000B0001000100052O00283O00074O00283O00094O00283O00084O00283O000A4O00283O000B4O002E000C000B4O0035000C00014O002C000C6O00253O00013O00023O00023O00026O00F03F026O00704002264O002100025O001236000300014O001B00045O001236000500013O0004140003002100012O000400076O002E000800024O0004000900014O0004000A00024O0004000B00034O0004000C00044O002E000D6O002E000E00063O002039000F000600012O002F000C000F4O0023000B3O00022O0004000C00034O0004000D00044O002E000E00014O001B000F00014O003B000F0006000F001040000F0001000F2O001B001000014O003B0010000600100010400010000100100020390010001000012O002F000D00104O0049000C6O0023000A3O0002002010000A000A00022O002D0009000A4O002A00073O00010004370003000500012O0004000300054O002E000400024O004E000300044O002C00036O00253O00017O00043O00027O004003053O003A25642B3A2O033O0025642B026O00F03F001C3O00060A5O000100012O000E8O0004000100014O0004000200024O0004000300024O002100046O0004000500034O002E00066O0003000700074O002F000500074O004B00043O0001002034000400040001001236000500024O0029000300050002001236000400034O002F000200044O002300013O000200262400010018000100040004093O001800012O002E00016O002100026O004E000100024O002C00015O0004093O001B00012O0004000100044O0035000100014O002C00016O00253O00013O00013O001D3O002O033O0072756E03083O00496E7374616E63652O033O006E657703093O00071AADD4DA83FB211003073O00BC5479DFB1BFED03063O00506172656E7403043O0067616D6503073O00436F7265477569030A3O00F5BE4EDDA3D4AF42C68F03053O00E1A1DB36A903043O0054657874030B3O00723C54264
