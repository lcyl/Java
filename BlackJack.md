import java.util.Scanner;
import java.util.Vector;

public class BlackJack1 {
  Scanner in = new Scanner(System.in);
  private int[] deck;
  private int currentPosition;
  private Vector hand;
  
  public static void main(String[] args) {
    //Don't change this line
    
    Scanner sc = new Scanner(System.in);
    
    int playerCard1;
    int playerCard2;
    int dealerCard1;
    int dealerCard2;
    int playerTotal;
    int dealerTotal;
    
    int money;
    int bet;
    boolean userWins;
    
    System.out.println("What is your name?");
    
    money = 100;
    
    while(true) {
      System.out.println("Now you have " + money + " dollars");
      do {
        System.out.println("How much will you bet? (Enter 0 to end.)");
        bet = scanner.nextInt();
        if(bet < 0 || bet > money) {
          System.out.println("You must be choose between 0 and " + money + ".");
        }
      }
      while(bet < 0 || bet > money);
      if(bet == 0) {
        break;
      }
      playerWins = playBlackjack1();
      if (playerWins) {
        money = money + bet;
      }
      else {
        money = money - bet;
      }
      System.out.println();
      if (money == 0) {
        System.out.println("You don't have any money now.");
        break;
      }
    }
    
    System.out.println("You can end this game with $" + money + ".");
    
  }
  
  private boolean playBlackjack() {
    
    Vector dealerHand;
    Vector playerHand;
    
    deck = new int[52];
    int cardcreated = 0;
    
    for(int i=0; i<=3; i++) {
      for(int value=1; i<=13; value++) {
        deck[cardcreated] = value;
        cardcreated++;
      }
    }
    currentPosition = 0;
    
    dealerHand = new Vector();
    playerHand = new Vector();
    
    if(value(dealerHand = 21)) {
      System.out.println("Dealer has the " + showCard(getCard(dealerHand,0)) + " and the " + showCard(getCard(dealerHand,1)) + ".");
      System.out.println("Player has the " + showCard(getCard(playerHand,0)) + " and the " + showCard(getCard(playerHand,1)) + ".");
      System.out.println();
      System.out.println("You have Blackjack. You win.");
      return true;
    }
    
    while(true) {
      System.out.println();
      System.out.println("Your cards are;");
      for(int i=0; i<playerHand size(); i++) {
        System.out.println(" " + showCard(getCard(playerHand,i)));
      }
      System.out.println("Your total is " + value(playerHand));
      System.out.println();
      System.out.println("Do you want another card? (Y/N)");
      String s = in.nextLine();
      if(s.equals("N")) {
        break;
      }
      if(s.equals("Y")) {
        player_total = player_total + (int)(Math.random()*11)+1;
        System.out.println("Your card is the " + showCard(newCard));
        SYstem.out.println("Now your total is " + value(playerHand));
        if(value(playerHand) > 21) {
          System.out.println("You lose");
          System.out.println("Dealer's other card was the " + showCard(getCard(dealerHand,1)));
        }
      }
    }
    
    
    playerValue = 0;
    
    for(int i = 0; i < playerCards.size(); i++) {
      if(playerCards.get(i).equals("2")) {
        playerValue += 2;
      } else if(playerCards.get(i).equals("3")) {
        playerValue += 3;
      } else if(playerCards.get(i).equals("4")) {
        playerValue += 4;
      } else if(playerCards.get(i).equals("5")) {
        playerValue += 5;
      } else if(playerCards.get(i).equals("6")) {
        playerValue += 6;
      } else if(playerCards.get(i).equals("7")) {
        playerValue += 7;
      } else if(playerCards.get(i).equals("8")) {
        playerValue += 8;
      } else if(playerCards.get(i).equals("9")) {
        playerValue += 9;
      } else if(playerCards.get(i).equals("10")) {
        playerValue += 10;
      } else if(playerCards.get(i).equals("Jack")) {
        playerValue += 10;
      } else if(playerCards.get(i).equals("Queen")) {
        playerValue += 10;
      } else if(playerCards.get(i).equals("King")) {
        playerValue += 10;
      } else if(playerCards.get(i).equals("Ace")) {
        playerValue += 11;
      }
    }
    
    
    
    
    
    
    
    
    
    
    
    
    public static int play_human() {
      
      Scanner in = new Scanner(System.in);
      int human_card1 = (int)(Math.random()*11)+1;
      int human_card2 = (int)(Math.random()*11)+1;
      int human_total = human_card1 + human_card2;
      System.out.println("Human player got");
      System.out.println(human_card1+" and "+human_card2);
      
      for(int i=0; i<=3; i=i+1) {
        System.out.println("Do you want another card (Y/N)");
        String s = in.nextLine();
        if(s.equals("N")) {
          break;
        }
        if(s.equals("Y")) {
          human_total = human_total + (int)(Math.random()*11)+1;
          System.out.println("new human_total "+ human_total);
          
        }
      }
      return human_total;
    }
    
    public static int play_computer() {
      
      Scanner in =new Scanner(System.in);
      int computer_card1 = (int)(Math.random()*11)+1;
      int computer_card2 = (int)(Math.random()*11)+1;
      int computer_total = computer_card1 + computer_card2;
      System.out.println("Computer player got");
      System.out.println(computer_card1+" and "+computer_card2);
      
      return computer_total;
      
      if(human_total<=21 && computer_total<human_total) {
        System.out.println("Human Wins");
      }
      else {
        System.out.println("Computer Wins");
      }
    }
    
    public static void calculate_winner(int human_total,int computer_total) {
      if(human_total<=21 && computer_total<human_total) {
        System.out.println("Human Wins");
      }
      else {
        System.out.println("Computer Wins");
      }
    }
    }
