	# bool - yes or no ( true or false )
	# int, string, bool, object
	# ints, strings, bools, objects
	# none
	
	"로스트 아크" = { 
		"아이템" = { }
		"영웅" = { }
		"연마" = { }
		"재료" = { }
		"귀속" = { }

		"영웅 연마 재료"@"영웅"@"연마"@"재료"@bool = { }
		"획득시 귀속"@"귀속"@bool = { }
		"아이템 티어"@int@1@2 = { } 
		"설명"@string = { }
		"분해불가"@bool = { }
		"획득처"@objects = { }
		"사용처"@objects = { }

		"단단한 은 광석" = { }
		"섬" = { }
		"채광" = { }
		"지는 너울의 대검" = { }
		"제작" = { }

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
	}

	"로스트 아크"-"아크라시움2"@"로스트 아크"-"아이템" = { 
		"로스트 아크"-"아크라시움2" = "로스트 아크"-"아크라시움1" # copy
		"로스트 아크"-"아이템 티어" = 2
		"로스트 아크"-"설명" = '장비를 연마하는데 필요한 재료. 특정 아이템 레벨의 장비를 연마할 수 있다'
		"로스트 아크"-"획득처" = {
			#
		}
		"로스트 아크"-"사용처" = {
			#
		}
	}
#
	"A" = { } # empty data?
	"B"@"A" = { 
		"a" = 3
		"b" = 4
	}
	"E"@"B" = {
		"b" = 5
	}
	"F"@"B"@"E" = { # => "F"@"E"? or error!

	}

	"a"@int = { }
	"b"@int = { }
	"d"@ints = { }

	"namespace" = {
		"a"@int = { }
	}

	"c_a"@int = 3
	"c_b"@const@int = 5

	"X" = { 
		"namespace"-"a" = 1
		"a" = 5
		"b" = "c_b"
		"a" = "c_a"
		"d" = { 4 5 6 7 }
	}

