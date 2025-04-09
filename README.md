# dsfunction showFinalScreen() {
            gameScreen.classList.add('hidden');
            finalScreen.classList.remove('hidden');
            finalScoreDisplay.textContent = score;
            
            // Վերջնական հաղորդագրություն՝ ըստ միավորների
            const maxScore = scenarios.length * 10;
            
            if (score >= maxScore * 0.8) {
                finalMessage.textContent = "Հիանալի է! Դու հասկանում ես, թե ինչպես պետք է կանխել բուլինգը և օգնել ուրիշներին:";
            } else if (score >= maxScore * 0.6) {
                finalMessage.textContent = "Լավ արդյունք! Դու հիմնականում գիտես, թե ինչպես պետք է վարվել բուլինգի հետ կապված իրավիճակներում:";
            } else if (score >= maxScore * 0.4) {
                finalMessage.textContent = "Միջին արդյունք: Փորձիր ավելի զգայուն լինել բուլինգի նկատմամբ և ավելի հաճախ միջամտել:";
            } else {
                finalMessage.textContent = "Քեզ անհրաժեշտ է ավելի շատ սովորել բուլինգի մասին: Հիշիր, որ աջակցությունն ու միջամտությունը շատ կարևոր են:";
            }
            
            // Թարմացնել առաջընթացի տողը
            progressBar.style.width = '100%';
            progressBar.textContent = '100%';
        }
        
        // Վերսկսելու կոճակի իրադարձություն
        restartBtn.addEventListener('click', () => {
            gameScreen.classList.remove('hidden');
            finalScreen.classList.add('hidden');
            startGame();
        });
    </script>
</body>
</html>
