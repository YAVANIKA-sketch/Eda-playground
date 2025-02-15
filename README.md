# d flip flop verilog code
module dff(q,qbar,d,set,rst,clk);
  input d,set,rst,clk;
  output reg q;
  output qbar;
  assign qbar=~q;
  always@(posedge clk or negedge set or negedge rst)
    begin
      if(rst==0)
        q=0;
      else if (set==0)
      q=1;
      else
        q=d;
    end
endmodule
