module PC(PC_current , clk , reset ,PC_final);
input clk;
input reset;
input [31:0]PC_final;
output reg [31:0]PC_current;


always@(negedge clk or posedge reset)
begin
if (reset)
begin
PC_current <= 32'b0;
end
else if(!reset)
begin
PC_current<=PC_final;
end
end

endmodule

