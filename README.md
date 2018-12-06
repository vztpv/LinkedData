
"아이템" = { interface }
"영웅" = { interface }
"연마" = { interface }
"재료" = { interface }
"귀속" = { interface }

bool = { no yes } # default : no

"영웅 연마 재료"@"영웅"@"연마"@"재료" = { bool }
"획득시 귀속"@"귀속" = { bool }
"아이템 티어" = { int 1 2 }
"설명" = { string }
"분해불가" = { bool }
"획득처" = { objects }
"사용처" = { objects }

"아크라시움1"@"아이템" = { 
	"영웅 연마 재료" = yes
	"획득시 귀속" = yes
	"아이템 티어" = 1
	"설명" = '장비를 연마하는데 필요한 재료. 특정 아이템 레벨의 장비를 연마할 수 있다'
	"분해불가" = yes
	"획득처" = {
		# for test, just one.. 
		"단단한 은 광석"&"섬"&"채광" # related_object?
	}	
	"사용처" = {
		# for test, just one..
		"지는 너울의 대검"&"제작"
	}
}
