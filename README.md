package h;

import java.util.ArrayList;
import java.util.Collections;
import java.util.Comparator;
import java.util.Scanner;

public class col {

	private ArrayList<hhh> ha = new ArrayList<hhh>();

	public void print() {
		for(hhh item : ha)
		{   
		      System.out.println(item.getNum()
		                       + " "
		                       + item.getNum()
		                       );
		}

	}

	public void setnumber(String s) {

		
		hhh l = new hhh(s, s+"1");
		ha.add(l);
	}

	public void sort() {
		// ha.sort(null);
		Collections.sort(ha, new Comparator<hhh>(){
		    public int compare(hhh s1, hhh s2) {
		        return s1.getNamik().compareToIgnoreCase(s2.getNamik());
		    }
		});
	}

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		col m=new col();
		Scanner s = new Scanner(System.in);
		while (s.hasNextLine()) {
			String number = s.nextLine();
			// double g= Double.parseDouble(number);
			// l.ha.add(g);
			// Collections.sort(l.ha);
			m.setnumber(number);
			m.sort();
			m.print();
		}
		s.close();
		System.exit(0);
		;
	}

}
