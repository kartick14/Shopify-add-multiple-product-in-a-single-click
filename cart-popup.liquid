<a class="btn btn-warning" id="go-update" onclick="updateDelvDate();" style="background: #e60f8c;">Update</a>
<script> 
 function updateDelvDate(){
    var delivery_dates = jQuery('.day-picker-all-days li.active').attr('data-day');
    var zip = $('[name="zip"]').val();
    
    if(jQuery('.day-picker-all-days li.active').length > 0) {           
      var dataitems = '';
      var count = 0;
      var cartdata = '';
      $.getJSON( "/cart.js", function( data ) {       
        cartdata = data.items;
          $.ajax({
              type: "GET",
              url: '/cart/clear.js',
              data: '',
              dataType: 'json',
              success: function(datam) { 
                  console.log(cartdata);
                var arraystr = '';
                var arrayqty = '';
		if(cartdata.length > 0){
			$.each( cartdata, function( key, val ) {    
			  arraystr = arraystr + val.id + ','; 
			  arrayqty = arrayqty + val.quantity + ','; 
			});
		}
                    addAllItems(arraystr,arrayqty);
                 /* $.each( cartdata, function( key, val ) {                
                    $.ajax({
                      type: 'POST',                             
                      url: '/cart/add.js',
                      dataType: 'json',                               
                      data: {quantity: val.quantity, id: val.id, properties: {'Delivery Date': $('.txt-regular.active').data('day')}},
                      success: function(response){                        
                        count++;
                        if(count == cartdata.length){
                          //location.reload();
                          setTimeout(location.reload(), 15000);
                        }
                        //console.log(count);
                        //console.log(response);
                      }                       
                    });
                  });*/
              }
          });           
      });      
      
    }else{
        alert('Please select a date.');
    }
  }
  
  function addAllItems(array,arrayqty){
    //var array = '99792519180,99803136012,99806576652,99807133708,99786850316,99856220172';
    Shopify.queue = [];
    var quantity = 0;
    var quantityar = arrayqty.split(',');;
    var newArray = array.split(',');
    for (var i = 0; i < newArray.length; i++) {
        product = newArray[i];
        productqty = quantityar[i],
        Shopify.queue.push({
            variantId: product,
            variantQty: productqty,
        });
    }
    
    Shopify.moveAlong = function() {
        // If we still have requests in the queue, let's process the next one.
        if (Shopify.queue.length) {
            var request = Shopify.queue.shift();
            var data = 'id='+ request.variantId + '&quantity='+request.variantQty
            $.ajax({
                type: 'POST',
                url: '/cart/add.js',
                dataType: 'json',
                data: {quantity: request.variantQty, id: request.variantId, properties: {'Delivery Date': $('.txt-regular.active').data('day')}},
                success: function(res){
                    Shopify.moveAlong();
                    quantity += 1;
                },
                error: function(){
                    // if it's not last one Move Along else update the cart number with the current quantity
                    if (Shopify.queue.length){
                        Shopify.moveAlong()
                    } else {
                      console.log('err-quantity: '+quantity);
                      setTimeout(location.reload(), 15000);
                        //$('#cart-number').replaceWith("<a href="/cart" id="cart-number">View cart (" + quantity + ")</a>")
                    }
                }
            });
        }
        // If the queue is empty, we add 1 to cart
        else {
            quantity += 1;
            addToCartOk(quantity);
        }
    };
    Shopify.moveAlong();
};


function addToCartOk(quantity){  
  console.log('succ-quantity: '+quantity);
  setTimeout(location.reload(), 15000);
    //$('#cart-number').replaceWith("<a href="/cart" id="cart-number">View cart (" + quantity + ")</a>");
} 
</script>
