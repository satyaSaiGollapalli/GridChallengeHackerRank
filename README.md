# GridChallengeHackerRank

Given a square grid of characters in the range ascii[a-z], rearrange elements of each row alphabetically, ascending. Determine if the columns are also in ascending alphabetical order, top to bottom. Return YES if they are or NO if they are not.



public static String gridChallenge(List<String> grid) {
    // Write your code here
        int n=grid.size();
        if(n==1)
        {
            return "YES";
        }
        for(int i=0;i<n-1;i++){
            String a=grid.get(i);
            String b=grid.get(i+1);
            char [] aa=a.toCharArray();
            char [] bb=b.toCharArray();
            Arrays.sort(aa);
            Arrays.sort(bb);
            String c=new String(aa);
            String d=new String(bb);
            /*if(c.compareTo(d)>0)
            {
                //System.out.println("n");
                return "NO";
            }*/
            for(int x=0;x<c.length();x++)
            {
                if(c.charAt(x)>d.charAt(x))
                {
                    return "NO";
                }
            }
        }
        System.out.println("y");
        return "YES";
    }

}
