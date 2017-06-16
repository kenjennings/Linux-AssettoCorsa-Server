# Linux-AssettoCorsa-Server
Lame tools for managing the server.

# ac
stupid script for launching the server, so I don't have to remember nohup blah de blah.

# acpick 
WORK IN PROGRESS

5/26 --The script examines the content directories on the server and enumerates all the tracks and cars available.   Eventually this will allow the user to choose a track and car and quickly rewrite the server config file....

5/29 -- Some improvements.  The scope for the arrays for track names and card names is fixed.

The script allows choice of track name (and car) and will rebuild the server_cfg.ini file using that chosen track.

Note that it only goes through the motion of choosing a car.  It turns out the car selection is more complicated and will require more thought.  The car names put into server_cfg.ini must match entries in the entry_list.ini file which describes individual cars.  So, this will need modification to build both files.

Also TO-DO -- On further testing it appears track names with a blank CONFIG_TRACK value are only valid if there is no other entry for that same track with a non-blank CONFIG_TRACK setting.  Therefore, the script needs to be modified to eliminate the blank CONFIG_TRACK entries when a subsequent non-blank CONFIG track is added.

# acpick.txt
Example output from an earlier version of the script enumerating the tracks and track variations, and the available cars.  Note that the track list is technically not correct.  See note above about CONFIG_TRACK blank and non-blank value for the reason.  However, this is good enough to see the specific names of tracks and optional layouts which is needed for the server config file.

TRACKS:
1  -  drift    
2  -  imola    
3  -  ks_barcelona    
4  -  ks_black_cat_county    
5  -  ks_black_cat_county     layout_int
6  -  ks_black_cat_county     layout_long
7  -  ks_black_cat_county     layout_short
8  -  ks_brands_hatch    
9  -  ks_drag    
10  -  ks_drag     drag1000
11  -  ks_drag     drag200
12  -  ks_drag     drag2000
13  -  ks_drag     drag400
14  -  ks_drag     drag500
15  -  ks_highlands    
16  -  ks_highlands     layout_drift
17  -  ks_highlands     layout_int
18  -  ks_highlands     layout_long
19  -  ks_highlands     layout_short
20  -  ks_monza66    
21  -  ks_monza66     full
22  -  ks_monza66     junior
23  -  ks_monza66     road
24  -  ks_nordschleife    
25  -  ks_nurburgring    
26  -  ks_nurburgring     layout_gp_a
27  -  ks_nurburgring     layout_gp_b
28  -  ks_nurburgring     layout_sprint_a
29  -  ks_nurburgring     layout_sprint_b
30  -  ks_red_bull_ring    
31  -  ks_silverstone    
32  -  ks_silverstone     gp
33  -  ks_silverstone     international
34  -  ks_silverstone     national
35  -  ks_silverstone1967    
36  -  ks_vallelunga    
37  -  ks_vallelunga     classic_circuit
38  -  ks_vallelunga     club_circuit
39  -  ks_vallelunga     extended_circuit
40  -  ks_zandvoort    
41  -  magione    
42  -  monza    
43  -  mugello    
44  -  spa    
45  -  trento-bondone    

CARS:
1  -  abarth500
2  -  abarth500_s1
3  -  alfa_romeo_giulietta_qv
4  -  alfa_romeo_giulietta_qv_le
5  -  bmw_1m
6  -  bmw_1m_s3
7  -  bmw_m3_e30
8  -  bmw_m3_e30_drift
9  -  bmw_m3_e30_dtm
10  -  bmw_m3_e30_gra
11  -  bmw_m3_e30_s1
12  -  bmw_m3_e92
13  -  bmw_m3_e92_drift
14  -  bmw_m3_e92_s1
15  -  bmw_m3_gt2
16  -  bmw_z4
17  -  bmw_z4_drift
18  -  bmw_z4_gt3
19  -  bmw_z4_s1
20  -  ferrari_312t
21  -  ferrari_458
22  -  ferrari_458_gt2
23  -  ferrari_458_s3
24  -  ferrari_599xxevo
25  -  ferrari_f40
26  -  ferrari_f40_s3
27  -  ferrari_laferrari
28  -  ks_abarth500_assetto_corse
29  -  ks_abarth_595ss
30  -  ks_abarth_595ss_s1
31  -  ks_abarth_595ss_s2
32  -  ks_alfa_mito_qv
33  -  ks_alfa_romeo_155_v6
34  -  ks_alfa_romeo_4c
35  -  ks_alfa_romeo_gta
36  -  ks_audi_a1s1
37  -  ks_audi_r8_lms
38  -  ks_audi_r8_plus
39  -  ks_audi_sport_quattro
40  -  ks_audi_sport_quattro_rally
41  -  ks_audi_sport_quattro_s1
42  -  ks_bmw_m235i_racing
43  -  ks_bmw_m4
44  -  ks_bmw_m4_akrapovic
45  -  ks_corvette_c7r
46  -  ks_corvette_c7_stingray
47  -  ks_ferrari_488_gt3
48  -  ks_ferrari_488_gtb
49  -  ks_ferrari_f138
50  -  ks_ferrari_fxx_k
51  -  ks_ferrari_sf15t
52  -  ks_ford_escort_mk1
53  -  ks_ford_gt40
54  -  ks_ford_mustang_2015
55  -  ks_glickenhaus_scg003
56  -  ks_lamborghini_aventador_sv
57  -  ks_lamborghini_countach
58  -  ks_lamborghini_countach_s1
59  -  ks_lamborghini_gallardo_sl
60  -  ks_lamborghini_gallardo_sl_s3
61  -  ks_lamborghini_huracan_gt3
62  -  ks_lamborghini_huracan_st
63  -  ks_lamborghini_miura_sv
64  -  ks_lotus_25
65  -  ks_lotus_72d
66  -  ks_maserati_250f_12cyl
67  -  ks_maserati_250f_6cyl
68  -  ks_maserati_gt_mc_gt4
69  -  ks_maserati_levante
70  -  ks_mazda_787b
71  -  ks_mazda_miata
72  -  ks_mazda_mx5_cup
73  -  ks_mazda_mx5_nd
74  -  ks_mazda_rx7_spirit_r
75  -  ks_mazda_rx7_tuned
76  -  ks_mclaren_650_gt3
77  -  ks_mclaren_f1_gtr
78  -  ks_mclaren_p1
79  -  ks_mercedes_190_evo2
80  -  ks_mercedes_amg_gt3
81  -  ks_mercedes_c9
82  -  ks_nissan_370z
83  -  ks_nissan_gtr
84  -  ks_nissan_gtr_gt3
85  -  ks_nissan_skyline_r34
86  -  ks_porsche_718_boxster_s
87  -  ks_porsche_718_boxster_s_pdk
88  -  ks_porsche_718_cayman_s
89  -  ks_porsche_718_spyder_rs
90  -  ks_porsche_908_lh
91  -  ks_porsche_911_carrera_rsr
92  -  ks_porsche_911_gt1
93  -  ks_porsche_911_gt3_cup_2017
94  -  ks_porsche_911_gt3_rs
95  -  ks_porsche_911_gt3_r_2016
96  -  ks_porsche_911_r
97  -  ks_porsche_911_rsr_2017
98  -  ks_porsche_917_30
99  -  ks_porsche_917_k
100  -  ks_porsche_918_spyder
101  -  ks_porsche_919_hybrid_2015
102  -  ks_porsche_919_hybrid_2016
103  -  ks_porsche_935_78_moby_dick
104  -  ks_porsche_962c_longtail
105  -  ks_porsche_962c_shorttail
106  -  ks_porsche_991_carrera_s
107  -  ks_porsche_991_turbo_s
108  -  ks_porsche_cayenne
109  -  ks_porsche_cayman_gt4_clubsport
110  -  ks_porsche_cayman_gt4_std
111  -  ks_porsche_macan
112  -  ks_porsche_panamera
113  -  ks_praga_r1
114  -  ks_ruf_rt12r
115  -  ks_ruf_rt12r_awd
116  -  ks_toyota_ae86
117  -  ks_toyota_ae86_drift
118  -  ks_toyota_ae86_tuned
119  -  ks_toyota_gt86
120  -  ktm_xbow_r
121  -  ks_toyota_supra_mkiv
122  -  ks_toyota_supra_mkiv_drift
123  -  ks_toyota_supra_mkiv_tuned
124  -  lotus_2_eleven
125  -  lotus_2_eleven_gt4
126  -  lotus_49
127  -  lotus_98t
128  -  lotus_elise_sc
129  -  lotus_elise_sc_s1
130  -  lotus_elise_sc_s2
131  -  lotus_evora_gtc
132  -  lotus_evora_gte
133  -  lotus_evora_gte_carbon
134  -  lotus_evora_gx
135  -  lotus_evora_s
136  -  lotus_evora_s_s2
137  -  lotus_exige_240
138  -  lotus_exige_240_s3
139  -  lotus_exige_s
140  -  lotus_exige_scura
141  -  lotus_exige_s_roadster
142  -  lotus_exige_v6_cup
143  -  lotus_exos_125
144  -  lotus_exos_125_s1
145  -  mclaren_mp412c
146  -  mclaren_mp412c_gt3
147  -  mercedes_sls
148  -  mercedes_sls_gt3
149  -  p4-5_2011
150  -  pagani_huayra
151  -  pagani_zonda_r
152  -  ruf_yellowbird
153  -  shelby_cobra_427sc
154  -  tatuusfa1
155  -  ks_mclaren_p1_gtr
156  -  ks_toyota_celica_st185
157  -  ks_toyota_ts040
158  -  ks_mclaren_570s
159  -  ks_audi_tt_vln
160  -  ks_lotus_3_eleven
161  -  ks_maserati_mc12_gt1
162  -  ks_audi_tt_cup
163  -  ks_audi_r18_etron_quattro
164 - ks_audi_r8_lms_2016
