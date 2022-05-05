import java.util.Scanner;
import java.util.*;
public class Main
{    
    public static void main(String[] args)
    {
        Constructor pass = allWords.pass();

        Main.analysis(pass);

        Scanner input = new Scanner(System.in);
        boolean keepGoing = true;

        while(keepGoing)
        {
            System.out.println();
            System.out.println("Would you like to go again?");
            System.out.println("1. Yes");
            System.out.println("2. No");
            System.out.println();

            int numInput = input.nextInt();

            if (numInput == 1)
            {
                for (int x = 0; x < 50; x ++)
                {
                    System.out.println();
                }
                Main.analysis(pass);
            }

            if (numInput == 2)
            {
                keepGoing = false;
                System.out.println();
                System.out.println("See you later!");
            }
            
        }
    }

    public static void analysis(Constructor pass)
    {
        boolean cancel = false;
        int numInput;
        char charInput;
        String letter;
        boolean keepGoing = true;
        String letter1 = "_";
        String letter2 = "_";
        String letter3 = "_";
        String letter4 = "_";
        String letter5 = "_";

        Scanner input = new Scanner(System.in);

        ArrayList<String> sortedArray = new ArrayList<String>(pass.getWordArray());
        //ArrayList<String> unSortedArray = new ArrayList<String>(pass.getWordArray());
        //System.out.println(pass.getWordArray().size());
        //System.out.println(sortedArray.size());

        while(keepGoing)
        {
            String inpWord = "[" + letter1 + letter2 + letter3 + letter4 + letter5 + "]";
            
            System.out.println();
            System.out.println("Found Letters: " + inpWord);
            System.out.println();
            System.out.println("Words Remaining: " + sortedArray.size());
            System.out.println("Choose a task");
            System.out.println("1. Word does not include letter");
            System.out.println("2. Word includes letters / where letters are not");
            System.out.println("3. Input where letters are");
            System.out.println("4. Print words remaining");
            System.out.println("5. Quit");
            System.out.println();

            numInput = input.nextInt();
            if (numInput == 1) //Word does not include letter
            {
                int stringLength = 0;
                String letters = "";
                ArrayList<String> letterList = new ArrayList<String>();

                System.out.println();
                System.out.println("Words Remaining: " + sortedArray.size());
                System.out.println("What letter(s)?");

                letters = input.next();
                stringLength = letters.length();

                for (int i = 0; i < stringLength; i++)
                {
                    char oneLetterNow = letters.charAt(i);
                    String oneLetter = Character.toString(oneLetterNow);
                    letterList.add(oneLetter);
                }
                //System.out.println(letterList);

                for(int i = 0; i < letterList.size(); i++)
                {
                    String oneLetter = letterList.get(i);
                    for (int y = 0; y < sortedArray.size(); y++)
                    {
                        if (sortedArray.get(y).contains(oneLetter))
                        {
                            sortedArray.remove(y);
                            i = -1;
                        }
                    }
                }
                for (int x = 0; x < 50; x ++)
                {
                    System.out.println();
                }
            }

            if (numInput == 2) //Word includes letter
            {
                System.out.println();
                System.out.println("Words Remaining: " + sortedArray.size());
                System.out.println("How many letters?");

                int runTimes = input.nextInt();

                for (int j = 0; j < runTimes; j++)
                {
                    System.out.println();
                    System.out.println("What letter?");

                    charInput = input.next().charAt(0);
                    letter = Character.toString(charInput);

                    System.out.println();
                    System.out.println("What position? (1-5)");
                    int posInput = input.nextInt();
                    posInput--;

                    for (int i = 0; i < sortedArray.size(); i++)
                    {
                        if (!sortedArray.get(i).contains(letter))
                        {
                            sortedArray.remove(i);
                            i = -1;
                        }
                    }

                    for (int i = 0; i < sortedArray.size(); i++)
                    {
                        String checkWord = sortedArray.get(i);
                        char c1 = checkWord.charAt(posInput);
                        String check = Character.toString(c1);

                        if (check.equals(letter))
                        {
                            sortedArray.remove(i);
                            i = -1;
                        }
                    }
                }
                for (int x = 0; x < 50; x ++)
                {
                    System.out.println();
                }
            }

            if (numInput == 3) //Position where letters are
            {
                System.out.println();
                System.out.println("Words Remaining: " + sortedArray.size());
                System.out.println("How many letters?");

                int runTimes = input.nextInt();

                for (int y = 0; y < runTimes; y++)
                {
                    System.out.println();
                    System.out.println("What letter?");
                    charInput = input.next().charAt(0);
                    letter = Character.toString(charInput);

                    System.out.println();
                    System.out.println("What position? (1-5)");
                    int posInput = input.nextInt();
                    
                    if (posInput == 1)
                    {
                        letter1 = letter.toUpperCase();
                    }
                    if (posInput == 2)
                    {
                        letter2 = letter.toUpperCase();
                    }
                    if (posInput == 3)
                    {
                        letter3 = letter.toUpperCase();
                    }
                    if (posInput == 4)
                    {
                        letter4 = letter.toUpperCase();
                    }
                    if (posInput == 5)
                    {
                        letter5 = letter.toUpperCase();
                    }
                    
                    posInput--;

                    for (int i = 0; i < sortedArray.size(); i++)
                    {
                        String checkWord = sortedArray.get(i);
                        char c1 = checkWord.charAt(posInput);
                        String check = Character.toString(c1);

                        if (!check.equals(letter))
                        {
                            sortedArray.remove(i);
                            i = -1;
                        }
                    }
                    
                }
                for (int x = 0; x < 50; x ++)
                {
                    System.out.println();
                }
            }

            if (cancel) //Position where letters are not (NOT USED ANYMORE)
            {
                System.out.println();
                System.out.println("What letter?");
                charInput = input.next().charAt(0);
                letter = Character.toString(charInput);

                System.out.println();
                System.out.println("What position? (1-5)");
                int posInput = input.nextInt();
                posInput--;

                for (int i = 0; i < sortedArray.size(); i++)
                {
                    String checkWord = sortedArray.get(i);
                    char c1 = checkWord.charAt(posInput);
                    String check = Character.toString(c1);

                    if (check.equals(letter))
                    {
                        sortedArray.remove(i);
                        i = -1;
                    }
                }
            }

            if (numInput == 4) //Print words remaining
            {
                for (int x = 0; x < 50; x ++)
                {
                    System.out.println();
                }
                if (sortedArray.size() > 20)
                {
                    System.out.println();
                    System.out.println("Too many words remaining");
                    System.out.println("Try to get rid of some");
                    System.out.println();
                }
                else
                {
                    System.out.println();
                    System.out.println("Words Remaining:");
                    System.out.println(sortedArray.toString());
                    System.out.println();
                }
            }

            if (numInput == 5) //Quit
            {
                keepGoing = false;
            }

            if (sortedArray.size() == 1)
            {
                keepGoing = false;
                System.out.println();
                System.out.println("Only one word remaining!");
                System.out.println("Your word is: " + sortedArray.get(0));
                System.out.println();
            }
            
            if (sortedArray.size() == 0)
            {
                keepGoing = false;
                System.out.println();
                System.out.println("No words remaining");
                System.out.println();
                System.out.println("Either you made an oopsie");
                System.out.println("or the word is not in the bank.");
                System.out.println("Let's hope it's the first one...");
                System.out.println();
            }
        }
    }
}
