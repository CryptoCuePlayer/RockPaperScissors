 if (userChoice.equals(computerChoice)) {
                System.out.println("Ничья!");
            } else if ((userChoice.equals("камень") && computerChoice.equals("ножницы")) ||
                    (userChoice.equals("ножницы") && computerChoice.equals("бумага")) ||
                    (userChoice.equals("бумага") && computerChoice.equals("камень"))) {
                System.out.println("Вы победили!");
            } else {
                System.out.println("Вы проиграли!");
            }
