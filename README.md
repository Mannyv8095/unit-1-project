present the game board

0 | 1 | 2
3 | 4 | 5
6 | 7 | 8

one player chooses a box to put his mark
player two chooses another box to put his mark

if player has (i && i+1 && i+2) or (i%3 == 0) or (i%3 == 1) or (i%3 == 2) or (i%4 == 0) or (i%2 == 0)
	then player wins


var player = 1;
//var player1Turn = [];
//var player2Turn = [];
//define all the column, row, and diagonal counts

while player === 1 {
   while (countFirstCol1 < 3 && countSecondCol1 < 3 && countThirdCol1 < 3 && countNWDiagonal1 < 3 && countNEDiagonal1 < 3 && countFirstRow1 < 3 && countSecondRow1 < 3 && countThirdRow1 < 3)
	for (each box on the board) {
		box.addEventHandler(‘click’,function(){
			add a symbol to the board
			//player1Turn.push(boxNumber);
		});

		if (boxNumber%3 === 0) {
			countFirstCol1++;
		} else if (boxNumber%3 === 1) {
			countSecondCol1++;
		} else if (boxNumber%3 === 2) {
			countThirdCol1++;
		} else if (boxNumber%4 === 0) {
			countNWDiagonal1++;
		} else if (boxNumber%2 === 0) {
			countNEDiagonal1++;
		} else if (boxNumber < 3) {
			countFirstRow1++;
		} else if (boxNumber > 2 && boxNumber < 6) {
			countSecondRow1++;
		} else if (boxNumber > 5 && boxNumber < 9) {
			countThirdRow1++;
		}

		determineWinner();
		player = 0;
	}
   }
}
while player === 0 {
	for (each box on the board) {
		box.addEventHandler(‘click’,function(){
			add a symbol to the board
			player2Turn.push(boxNumber);
		});
	}
	determineWinner();
	player = 1;
}
function determineWinner() {
	for (each entry in player1Turn) {
		if (entry%3 === 0) {
			countFirstCol++
		}
	}
}