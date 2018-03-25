package solution600;

import java.util.HashMap;
import java.util.HashSet;

public class solution599 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		String[] strings1 = {"Shogun", "Tapioca Express", "Burger King", "KFC"};
		String[] strings2 = {"Piatti", "The Grill at Torrey Pines", "Hungry Hunter Steakhouse", "Shogun"};
		String[] result = findRestaurant(strings1,strings2);
		
		for (String string : result) {
			System.out.println(string);
		}
	}
	
	public static String[] findRestaurant(String[] list1, String[] list2) {
        
		HashMap<String, Integer> map1 = new HashMap<String, Integer>();
		HashMap<String, Integer> map2 = new HashMap<String, Integer>();
		
		for (int i = 0; i < list1.length; i++) {
			String temp = list1[i];
			map1.put(temp, i);
		}
		
		for (int i = 0; i < list2.length; i++) {
			String temp = list2[i];
			map2.put(temp, i);
		}
		
		int sum = list1.length+list2.length;
		HashSet<String> set = new HashSet<String>();
		
		for (java.util.Map.Entry<String, Integer> entry : map1.entrySet()) {
			String key = entry.getKey();
			int value = entry.getValue();
			
			if (map2.containsKey(key)) {
				int index = map2.get(key);
				if (sum  >= value+index) {
					sum = Math.min(sum, value+index);
					set.add(key);
				}
			}
		}
		
		Object[] result = set.toArray();
		String[] results = new String[result.length];
		int i = 0;
		for (Object object : result) {
//			System.out.println(object);
			results[i++] = (String)object;
		}
		
		return results;
    }

}
